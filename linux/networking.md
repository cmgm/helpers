
# L3 interfaces  info 
ip addr show

# L2 interfaces  info 
ip link show

brctl show

brctl showmacs docker0

brctl showstp docker0

brctl show | awk 'NR > 1 {print "BRIDGE :[" $1 "]"}'

brctl show | awk 'NR > 1 {print " "$1" "}' | xargs -n 1 brctl showmacs
brctl show | awk 'NR > 1 {print " "$1" "}' | xargs -n 1 brctl showstp

brctl show | cut -f 1 | awk 'NR>1' | xargs -n 1 brctl showstp

brctl show | awk 'NR > 1 {print " "$1" "}' | tee -a  bridges1.txt && cat bridges1.txt | xargs echo

cat bridges1.txt |  tail -n +3

# Sockets
ss

# traffic capture 
tshark

