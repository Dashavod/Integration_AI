# Integrations ChatGPT to CRM

#### POST [Endpoint to Google Function](https://europe-central2-devtorium-qna.cloudfunctions.net/aihub)
Content-Type: application/json
```json
{
	"sender": "test_user",
	"message": "none",
	"type": "gpt",
	"key": "6Gb9tb29HC"
}
```

#### Errors
- Unautorized
![[Pasted image 20230303170801.png]]
- Wrong structure

***The model may return the answer in a slightly different structure, than you expected***
![[Pasted image 20230303171231.png]]

### Successful response example:
***each answer offten different, and provided information can be unreliable or irrelevant*
```json
{
	"Company type": "for profit",
	"Founded": 2012,
	"Headquarters": "Warsaw, Poland",
	"Industries": [
		"Retail",
		"Fashion",
		"Clothing",
		"Shoes",
		"Accessories"
	],
	"Info": "Sinsay is an online fashion retailer offering a wide range of clothing, shoes, and accessories for men, women, and children. Founded in 2012, the company has grown to become one of the leading fashion retailers in Europe. Sinsay offers a wide selection of products, including dresses, tops, jeans, shoes, and accessories. The company is committed to providing customers with fashionable and affordable clothing, and is focused on developing innovative solutions to meet the needs of its customers. Sinsay has been recognized for its commitment to sustainability, and was named one of the world's most sustainable companies.",
	"Mission": "Provide customers with fashionable and affordable clothing",
	"Number of employees": "Unknown",
	"Region": [
		"Europe",
		"Global"
	],
	"Revenue": "Unknown",
	"Technologies": [
		"AI",
		"Cloud",
		"Big Data"
	],
	"Values": "Innovation, Quality, and Customer Service",
	"headline": "Sinsay is an online fashion retailer offering a wide range of clothing, shoes, and accessories for men, women, and children.",
	"site": "sinsay.com"
}
```

***Firestore storage data in the same structure***

