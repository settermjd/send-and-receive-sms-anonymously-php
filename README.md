# Send and Receive SMS Anonymously with PHP and Twilio

<!-- markdownlint-disable MD013 -->
This privacy-conscious app uses a Twilio phone number to relay SMS messages to and from your phone, masking your phone number from the public.
For more details, see [Twilio's blog post about SMS forwarding][twilio_sms_forwarding_url].

## Prerequisites/Requirements

To run the code, you will need the following:

- PHP 8.3
- [Composer][composer_url] installed globally
- [ngrok][ngrok_url] and a free ngrok account
- A Twilio account (free or paid) with an active phone number that can send SMS.
  If you are new to Twilio, [create a free account][twilio_referral_url].

## Getting Started

After cloning the code to wherever you store your Go projects, and change into the project directory.
Then, copy _.env.example_ as _.env_, by running the following command:

```bash
cp -v .env.example .env
```

Then, set `MY_PHONE_NUMBER` to the phone number (in [E.164 format][twilio_e164_format_url]) that you want to receive SMS.

When that's done, run the following command to launch the application:

```php
go run main.go
```

Then, use ngrok to create a secure tunnel between port 8080 on your local development machine and the public internet, making the application publicly accessible, by running the following command.

```php
ngrok http 8080
```

## Contributing

If you want to contribute to the project, whether you have found issues with it or just want to improve it, here's how:

- [Issues][issues_url]: ask questions and submit your feature requests, bug reports, etc
- [Pull requests][pull_requests_url]: send your improvements

## Did You Find The Project Useful?

If the project was useful, and you want to say thank you and/or support its active development, here's how:

- Add a GitHub Star to the project
- Write an interesting article about the project wherever you blog

## License

[MIT][mit-license-url]

## Disclaimer

No warranty expressed or implied. Software is as is.

[composer_url]: https://getcomposer.org
[issues_url]: https://github.com/settermjd/send-and-receive-sms-anonymously-php/issues
[mit-license-url]: http://www.opensource.org/licenses/mit-license.html
[ngrok_url]: https://ngrok.com/
[pull_requests_url]: https://github.com/settermjd/send-and-receive-sms-anonymously-php/pulls
[twilio_e164_format_url]: https://www.twilio.com/docs/glossary/what-e164
[twilio_referral_url]: https://login.twilio.com/u/signup?state=hKFo2SA5Qlp2bThzaGh4T0RnUDJMU0c4VWxhZ0lYRUZrQlMxMqFur3VuaXZlcnNhbC1sb2dpbqN0aWTZIDVKUmh0dFM4ZTV0cmt2QkdKeVp6R212Z2JiMlE2U0R6o2NpZNkgTW05M1lTTDVSclpmNzdobUlKZFI3QktZYjZPOXV1cks
[twilio_sms_forwarding_url]: https://www.twilio.com/blog/sms-forwarding-and-responding-using-twilio-and-javascript
<!-- markdownlint-enable -->
