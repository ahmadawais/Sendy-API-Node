<h1 align="center">
  <img src="https://on.ahmda.ws/qrZY/c" />

  Sendy API for Node.js
</h1>


<br>



<table width='100%' align="center">
    <tr>
        <td align='left' width='100%' colspan='2'>
            <strong><code>Sendy API Node.js</code></strong><br />
            Node.js module for [Sendy API](http://sendy.co/api).
        </td>
    </tr>
    <tr>
        <td>
            A FOSS (Free & Open Source Software) project developed by <a href='https://github.com/ahmadawais'  target="_blank">Ahmad Awais</a>.
        </td>
        <td align='center'>
            <a  target="_blank" href='https://AhmadAwais.com/'>
                <img src='https://i.imgur.com/Asg4d3k.png' width='100' />
            </a>
        </td>
    </tr>
    <tr><td><sup> Follow Ahmad's #FOSS work on GitHub <a href='https://github.com/ahmadawais'>@AhmadAwais</a> —   Say Hi on Twitter <a href="https://twitter.com/mrahmadawais/">@MrAhmadAwais</a></sup></td><td  align='center'>👋</td></tr>
</table>

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/ahmadawais/Sendy-API-Node.svg?style=social&label=Stars)](https://github.com/ahmadawais/Sendy-API-Node/stargazers) [![GitHub followers](https://img.shields.io/github/followers/ahmadawais.svg?style=social&label=Follow)](https://github.com/ahmadawais?tab=followers) [![Tweet for help](https://img.shields.io/twitter/follow/mrahmadawais.svg?style=social&label=Tweet%20@MrAhmadAwais)](https://twitter.com/mrahmadawais/)

</div>

<br>

![Install](https://on.ahmda.ws/qsLN/c)

## Installation

Run the following command in your project.

```sh
npm i sendy-api-node
```

<br>

![Example](https://on.ahmda.ws/qsO2/c)

## Examples

First of all add this.

```js
var Sendy = require('sendy-api-node'),
    sendy = new Sendy('http://your_sendy_installation/', 'your_api_key');
```

<br>

![Example](https://on.ahmda.ws/qr5M/c)

## API

#### `subscribe`

```js
var params = {
    email: 'user@example.com',
    list_id: 'your_list_id'
}

sendy.subscribe(params, function(err, result) {
    if (err) console.log(err.toString());
    else console.log('Subscribed succesfully');
});
```

#### `unsubscribe`

```js
var params = {
    email: 'user@example.com',
    list_id: 'your_list_id'
}

sendy.unsubscribe(params, function(err, result) {
    if (err) console.log(err.toString());
    else console.log('Unsubscribed succesfully);
});
```

#### `status`

```js
var params = {
    email: 'user@example.com',
    list_id: 'your_list_id'
}

sendy.status(params, function(err, result) {
    if (err) console.log(err.toString());
    else console.log('Status: ' + result);
});
```

#### `countActive`

```js
var params = {
    list_id: 'your_list_id'
}

sendy.countActive(params, function(err, result) {
    if (err) console.log(err.toString());
    else console.log('Active subscribers: ' + result);
});
```

#### `createCampaign`

```js
var params = {
    from_name: 'Your name',
    from_email: 'email@example.com',
    reply_to: 'email@example.com',
    subject: 'Your Subject',
    plain_text: 'Campaign text'  // Optional.
    html_text: '<h1>Campaign text</h1>',
    send_campaign: 0 // Set to 0 if you just want to create a draft campaign — 1 if you want to create and send.
    list_ids: 'your_list_id' // seperate multiple lists with a comma. Only required if send_campaign parameter is true.
    brand_id: 'your_brand_id' // only required if send_campaign parameter is false. Check url what is, i=X that x is the brand ID.
};

sendy.createCampaign(params, function(err,result){
    if (err) console.log(err.toString());
    else console.log(result);
});
```

<br>

![License](https://on.ahmda.ws/qsw0/c)

## License & Attribution

**Licensed** as MIT ⓒ [Ahmad Awais](https://AhmadAwais.com/) — based on the initial fork of Igor Dimitrijevic's work.
