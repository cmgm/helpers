

# gsutil 

to access a  bucket on a project , copy  to  bucket
1-Stop the Vm 
2 -change premition for the vm for gcs
3- start the VM 
4 - remove the gsutils config cache on the VM 

```
cd ~
cd ./gsutils
rm -r *
```

copy  the files 
```
gsutil cp beam_experiences.ipynb gs:\\gmapsapi-1488981423944/beam_data_projects
```

