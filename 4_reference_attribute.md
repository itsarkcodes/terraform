# Referencing resource attribute in terraform

- We can use the output of one resource and use it as input for another resource  
Eg:  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/33788538-d3fb-41c8-8d51-ade8119fa06b)

- ```${}``` : This is called interpolation sequence, eg- ```${random_pet.my-pet.id}```

- Output:

![image](https://github.com/itsarkcodes/terraform/assets/87442305/9c028fc1-6cee-4c9d-b458-73fb04578c08)
