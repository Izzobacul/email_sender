# email_sender

email_sender is a simple library that works on top of SMTPlib to provide an easy-to-use interface for sending and recieving emails.  
The package has two main classes, which are Email and Mail.

## Mail
The Mail class is used to represent emails. It has no functions, and 4 parameters, which are `from`, the email of the sender, `to`, the email(s) of the recipient, `subject`, the subject of the email, and `body`, the content of the email.
## Email
The class is used to send emails. It has one function, "send", and takes the url to the email `server`, a `username` for that server, and a `password` for that server.
#### `send`
This function takes one parameter of type [`Mail`](#mail), which represents the message that is about to be sent.

## Example  
```
   import email_sender
   my_email = email_sender.Email("smtp.gmail.com", "username", "password")
   my_message = email_sender.Mail(sender = "me@gmail.com", to = "you@gmail.com", subject = 'Hello!", body =
   '''
   Hey man! How ya doin? It's been a while since we last talked.
   I hope to see you sonn!
   -G
   '''
   )
   my_email.send(my_message)
```
