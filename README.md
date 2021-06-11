1. Download letest image of csvserver from docker hub 
    docker pull infracloudio/csvserver:latest
2. execute the shell script gencsv.sh to generate csv data 
3. chage the permission of file which is generated by script 
    chmod +x /csvserver
    chmod +x /csvserver/inputdata
3. Run the container using pulled docker image 
    docker run -d -it -v /csvserver/inputdata:/csvserver/inputdata -e CSVSERVER_BORDER='Orange' -p 9393:9300 --name sachin infracloudio/csvserver /bin/bash -c "./csvserver inputdata"
4. check the dash board in localhost:9393 in browser 
