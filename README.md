( impalementing OAuth and OpenID mechanism for SSO ), steps we did : 

open github account > setting > developers settings > OauthApps > create new oauth app : 
1- add Application name
2- add Homepage URL
3- add Application description and Authorization callback URL then > Register Application 

- after that it will shows Clinet_id and Clinet Secret_id  

- After generating 'Basma App' settings using Oauth apps in github , we make this code using JavaScript language to implement it 
- NOTE :( the code is also uploaded in separete page in our project page in github as "JavaScribt" file )

const express = require('express')

const app = express()

app.get('/',(req, res) => {
    res.send('hello world')
})
app.get('/callback' , (req, res) => {
    res.send('it should have worked!')
})

app.listen(3000, () => {

    console.log('we are running on port 3000')
})


- then we will open github Documentation and follow the steps (https://docs.github.com/en/developers/apps/building-oauth-apps/authorizing-oauth-apps) 
- we will copy the link that is shown in github Documentation  : https://github.com/login/oauth/authorize
- we will add (?client_id="our application client id)
- then it will show the login page > authorize > thats all.
- Finally we got Verification message sent to my email alert me that there is third party access to the Account in Github .
