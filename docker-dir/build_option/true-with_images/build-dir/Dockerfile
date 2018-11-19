FROM  opavlova/tomcat
ENV OP_TEST=op_test
EXPOSE 8090
#USER op
#images are rebuilt


182.2182
1. Ok: docker-compose
-deploy
-re-deploy docker-compose
1.1
- --build=true
Result: OK - no additional tabs
1.2
- --build=false
Result: Ok - the same tabs are opened because the image is not re-built: Log, Inspection

2. Ok: docker-compose
-deploy
-down
-deploy again
1.1
- --build=true
Result: OK - no additional tabs
1.2
- --build=false
Result: Ok

3. notOk: docker-compose, Dockerfile
-deploy
-delete a container
-re-deploy
Result: not Ok (one more Log appears - old Log tab is in focus, old Inspection tab in focus when calling a new one - IDEA-155346)

4. Case1:
-deploy Dockerfile
-re-deploy
Result:  not Ok (one more Log appears, old Inspection is present)

4. Case3 - saving changes in the container(ports, volumes tabs) leads to the adding a new Log tab