

# environment variables -------------------------------------

env 
echo $PATH

export VAR_A=$(pwd) && echo $VAR_A

env | grep PATH | tr ":" "\n"

PATH="/path_new:"$PATH


# Disks
df -h 
du  -h ./venv/
du -c -h .

 Top directories Space used under the  / dir 
sudo du -a -h / | sort -n -r | head -n 5
sudo du -a -h $HOME | sort -n -r | head -n 20

sudo du -Sh | sort -rh | head -5

biggest file sizes 
find -type f -exec du -Sh {} + | sort -rh | head -n 5


# Create files -----------------------------------------------

```
cat << EoF > ./my-document.txt
Hello world
Have a nice day
EoF
```

# Permissions -------------------------------------------------


# Echo 
> echo $?



# Downloading a file

# WGET


### CURL 
> curl -o data.txt https://example.com/data.txt

### Uploading a file
> curl -F "file=@/path/to/local/file.txt" https://example.com/upload

### Sending data using HTTP POST
> curl -d "param1=value1&param2=value2" https://example.com/post

### Specifies the name of the file to which the data should be saved. For example, 
> curl -o data.txt https://example.com/data.txt 

### Saves the output with the same name as the remote file. For example:
> curl -O https://example.com/data.txt

### Sets a header for the request. For example:
> curl -H "Authorization: Bearer TOKEN" https://example.com/api

### Sets the username and password for the request. For example:
> curl -u username:password https://example.com/api 


### Set the URL of the authentication endpoint
AUTH_URL="https://example.com/auth"

### Set the credentials to use for authentication
USERNAME="user"
PASSWORD="pass"

### Use curl to authenticate and obtain a token
TOKEN=$(curl -s -X POST -H "Content-Type: application/json" -d '{"username": "'"$USERNAME"'", "password": "'"$PASSWORD"'"}' $AUTH_URL | jq -r '.token')

### Check if the token was obtained successfully
if [ -z "$TOKEN" ]; then
    echo "Failed to obtain authentication token"
    exit 1
fi

### Set the URL of the resource to access
RESOURCE_URL="https://example.com/resource"

### Use curl with the token to access the resource
curl -s -H "Authorization: Bearer $TOKEN" $RESOURCE_URL

#  ---------------------------------------------------------



# links 
https://github.com/PacktPublishing/Complete-Bash-Shell-Scripting-

https://github.com/jayant2014/Bash-Scripting

https://github.com/Md-MamunAbdulKayum/shell-scripting-examples


# ssh Create Add SSH Key 

ssh-keygen -t ed25519 -C "carlosgasparmartins@gmail.com" \
eval "$(ssh-agent -s)" \
ssh-add ~/.ssh/id_ed25519 \

