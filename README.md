# deploy-to-eks-using-github-actions
steps to deploy:
1. Create an EKS Cluster using this command:

eksctl create cluster --name eks-learning02 --region us-east-2 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. Then create .github folder and then create workflows folder inside .github folder 
3. create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets with AWS_SECRECT_KEYS and AWS_ACCESS_KEY in github repo
        Go to settings of repo
        click on secrets and variables
6. Now push or commit the code to the github reposittory and see the changes
7. TO GET THE DNS DOMAIN OF THE APPLICATION go to aws-cli on the system and  type
  1. cd .aws
  2. kubectl get pods
  3. kubetctl get service 
  copy the DNS name 
9. Test application by getting the dns name and going to a web browser



AFTER RUNNING THE APPLICATION
7.Clean up the resource 
  Run: 
  eksctl delete cluster --name eks-learning02
