
# info manipulation 


tr -s " " <orders.txt | cut -d " " -f 2,3,4


awk -F"   " '{print $2,$3,$4}' orders.txt
awk 'BEGIN{ FS=OFS="   "}NR==1 || $3>200 {print $3, $2, $4}' orders.txt

