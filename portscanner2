#! /bin/bash

hostfile=$1
port=$2
echo "ip,port"
for host in {1..254}; do
	timeout .1 bash -c "echo >/dev/tcp/$hostfile.$host/$port" 2>/dev/null &&
		echo "$hostfile.$host,$port"
done
