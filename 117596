//server
const express = require('express');
const bodyParser = require('body-parser');
//const ejs = require('ejs');

const app = express();

//Global Variable
let userList = [];

app.set('view engine', 'ejs');

app.use(bodyParser.urlencoded({extended:true}));

app.use(express.static('public'));
app.get('/', function(req, res){
	res.render('index', {dateTime: 'Today', newItem: userList});
});

app.post('/',function(req, res){
	userList.push(req.body.newItem);
	res.redirect('/');
});

app.listen(8080, function(){
	console.log('\nserver started on port 8080!\n');
});
