# imobicash

This is a cryptocurrency from where you can do transaction ,send imobicoin and recieve imobicoin.

## Setup

Clone The Repository .

```sh

https://github.com/sakshamapp/imobicash.git

```
## Start wallet 

Open Cloned folder through command prompt and run this command

```sh

walletd.exe config configs/imobicash.conf

```


to open wallet in local port use this command

```sh

walletd.exe config configs/imobicash.conf -local

```

after this command you will get access from 127.0.0.1:36151/json_rpc



1)Register In Imobicash :

        Api 		= http://www.imobicash.org//CreateAddress?name=[name]&password=[password]&mobile=[mobile]&email=[email]call_back=[url]
		Response 	=  {"Error":false  ,"Message": "Registered Successfully....","address": "address" } 
														OR
						 {"Error": "False" ,"Message": "error message" }
		
		URL         = http://example.com/ReceivingCallBack?username=email;
		
		
		
2)Send Transaction :

        Api 		= http://www.imobicash.org/SendTrnsaction?username=[email]&receiver=[receiver address]&sender=[sender address]&cr=[amount]

		Response 	=  {"Error": "False" ,"Message": "success"."Hash":"Transaction Hash" }
													OR
								{"Error": "False" ,"Message": "error message" }
		
		
2)Callback Response :
         Api 		=[call_back_url]&cr=[amount]&address=[receiver address]
         
		 
		 When any address get any amount ,callback send to the url given at registration time.
