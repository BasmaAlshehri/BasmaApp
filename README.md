# After generating 'Basma App' settings using Oauth apps in github , we make this code using JavaScript language to implement it

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
