# Enviar e-mails usando o js


Existe uma solução muito simples para isso. Siga as etapas a seguir para enviar e-mails do seu Gmail usando o node (nodemailer)

- Etapa 1: abra este link https://myaccount.google.com/security
- Etapa 2: ativar a autenticação de 2 fatores
- Etapa 3: Clique em App passwords logo abaixo da autenticação de 2 fatores
- Etapa 4: Nas opções de Selecionar aplicativo, selecione Outro e escreva o nome do aplicativo, pode ser qualquer nome como mycustomapp
- Etapa 5: Ele irá gerar a senha, copie a senha do pop-up e use o seguinte código.
- Etapa 6: Use essa senha copiada na seção Auth password

# Instale

                                                npm install nodemailer

  
# Use este código
<div align="center"><img src="https://github.com/jeovanedossantossantos/answers-to-my-questions/assets/60934938/4c62ff64-dfba-4dfb-8415-e84556d251ca"/></div>


#


```
var nodemailer = require('nodemailer');

var transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
        user: 'seu_email@gmail.com',
        pass: 'sua_senha_do_app'
    }
});

var mailOptions = {
    from: 'seu_email@gmail.com',
    to: 'email_de_quem_recebe_a_menssagem@gmail.com',
    subject: 'Sending Email using Node.js',
    text: 'That was easy!'
};

transporter.sendMail(mailOptions, function (error, info) {
    if (error) {
        console.log(error);
    } else {
        console.log('Email sent: ' + info.response);
    }
});


```
