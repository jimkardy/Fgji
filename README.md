One Liner
```bash 
curl -sSL -o ucompose https://github.com/jimkardy/Fgji/releases/latest/download/ucompose.txt && chmod +x ucompose && ./ucompose doctor
```
Udocker ucompose is a compose cli for udocker. 

When creating a comprese.yml, do it like you would create a docker-compose.yml, it will be automatically translated into udocker commands. 

Take note that not all the commands that docker has will work here, this scrip is targeting termux users who want compose features root less without the need of a karnel. 

Exemples 

```bash
./ucompose up -d

./ucompose start

./ucompose stop

./ucompose down
```
And many more... 
