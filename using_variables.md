* By default, if you dont provide any values in ```variable.tf```, When we run terraform apply we will be prompted values for each variables used in a interactive mode  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/b6b67f2a-6e69-4a55-a110-67d0291b3d35)

* If you dont want to provide values in an interactive mode, then we can also use of command line flags  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/cf5e7965-2b72-481a-8a4f-e22190e27eb9)

* We can alsoo use the Environment Variables    
![image](https://github.com/itsarkcodes/terraform/assets/87442305/3f625583-3893-42b9-a4e0-11229fc49d15)

* When we are dealing with a lots of variables, we can load values by making use of variable definition file Eg: ```terraform.tfvars```  
* This variable definition file can be named anything but should always end in either ```.tfvars``` or ```.tfvars.json```
![image](https://github.com/itsarkcodes/terraform/assets/87442305/55d04154-f8e4-4b26-82af-618d40810e97)

![image](https://github.com/itsarkcodes/terraform/assets/87442305/15bc71c9-480a-4006-ac82-86a922bd621a)
* If you use any other file name such ```variables.tfvars``` , you will need to pass it along with the command line flag called  
```-var-file variables.tfvars```    
![image](https://github.com/itsarkcodes/terraform/assets/87442305/50f7af48-b022-4b86-9a06-be5be2f35d61)

## Variable Definition Precedence Order  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/26924503-2678-4a91-a735-a055d276d7e7)












