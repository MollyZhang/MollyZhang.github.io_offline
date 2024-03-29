---
layout: post
excerpt: "Running jupyter notebook from a server and view the notebook in your laptop browser via ssh"
thumbnail: ""
error_message: "/img/error_message_jupyter_remote.png"
comments: true
---
### Here is how you run jupyter notebook from a server:  
> At the remote server:  
* `ssh username@remote-server-public-dns`  
* `jupyter notebook --no-broswer --port 8800`  

> At your laptop:  
* `ssh -NL 8888:localhost:8800 username@remote-server-public-dns`  
* Type the password to login the remote server.  
* Open your browser and navigate to localhost:8888, and you should be able to use the jupyter notebook accessing the files remotely on the server.  
* You might be asked a "token" in the browser and you can find the token displayed in the remote server bellow "jupyter notebook --no-browser".  

Finally, "ssh -NL" means "do not execute a remote command, instead fowarding 8888 local host connection to remote port 8800 in the remote server over the ssh secure channel".

### bug fixes
I have encountered a bug repeatively when using jupyter notebook this way, here is the errror message:
<div class="imgcap">
    <img src="{{ page.error_message }}" >
</div>

Fix:  
Jupyter notebook need to write to .ipynb_checkpoints, but it didn't have write access. Giving user write access solved this issue.
