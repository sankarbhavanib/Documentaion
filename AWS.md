##  To work on AWS box run from your downloads(wheere your downloaded *.pem file) folder 
```
chmod 400 bhavani.pem
ssh -i "bhavani.pem" ec2-user@ec2-52-38-92-225.us-west-2.compute.amazonaws.com
$sudo yum update -y
$sudo yum install -y httpd   ( to install httpd.apache.org )
$sudo service httpd start D3vT00lsR0cks
```

## To work on docker 
```
docker-machine ls                            ( to find out the docker machine name , in this case default)
docker-machine start default               (default   is my stage name , replace your stage name)
docker-machine env default                   (default   is my stage name , replace your stage name)
eval "$(docker-machine env default)"         (default   is my stage name , replace your stage name)
```
