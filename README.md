# Stripe-Payment-Gateway-API-Multibanco-

Use Stripe to accept payments using Multibanco, the most popular payment method in Portugal.

# API ENDPOINTS

POST - /api/newCustomer/  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - email

POST - /api/addNewCard/  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - cardNumber, cardExpMonth, cardExpYear, cardCVC, cardName, country, postal_code

GET - /api/viewAllCards/

POST - /api/updateCardDetails/  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - cardId

POST - /api/deleteCard/  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - cardId

POST - /api/createCharge/  
One Time Payment with New Card  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - oneTime:true, amount, cardNumber, cardExpMonth, cardExpYear, cardCVC, country, postal_code  
Payment with an existing card  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body - oneTime:false, amount, cardId, email
