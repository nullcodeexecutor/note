```shell
jps -l | grep 'xxxx' | awk '{print $1}'  | sed -e "s/^/kill  /g" | sh -
```
<br/>


#####杀死某个目录下的所有进程
```shell
KEY="$PWD"
PID=$(ps -ef | grep "$KEY" | grep -v "grep" | awk '{print $2}')
if [[ ! -z $PID ]] ; then
        echo "PID is:$PID"
        kill -9 $PID
fi
```
<br/>