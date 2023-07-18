Discovery
```bash
nmap -p <port> - script grpc-discovery <target>  
grpcurl -plaintext <target>:<port> list
```

Monitoring
```python
import grpc  

def intercept_call(client_call_details):  
	print(f"Method: {client_call_details.method}")  
	return grpc.request_call(client_call_details)  
	
channel = grpc.insecure_channel('<target>:<port>')  
intercepted_channel = grpc.intercept_channel(channel, intercept_call)
```
i