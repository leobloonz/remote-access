# remote-access

add to .zshrc

need install NGROK

usage: remoto [PORT]

```
function remoto {
port=$1;ip=$(ip a | grep '/24' | cut -d ' ' -f 6 | cut -d '/' -f 1);echo "Server HTTP Python ONLINE [ CTRL+C to BRAKE]: $ip:$port"; python3 -m http.server $port 2>/dev/null | ngrok http $port
}
```
