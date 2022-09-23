## if you can't refresh snap-store in Ubuntu 22

If you can't refresh snap-store from Ubuntu 22. Use the following commands.


```ps -e | grep snap-store #id blocking process``` 


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663945741515/7Z2m0sAi6.png align="left")

Pick id process.


```kill #id_process``` 

and...


```sudo snap refresh``` 



![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663945878341/3ubnmGf6z.png align="left")

DONE!

