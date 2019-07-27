## Host : AWS SES, us-west, oregon

```
swaks -server email-smtp.us-west-2.amazonaws.com:587 -tls --h-Subject: "Hello" --body 'Testing SMTP awesomness!' \
        --auth-user USERNAME \
        --auth-password PASSWORD \
        --from noreply@domain.com \
        --to YOUREMAIL@gmail.com
```
