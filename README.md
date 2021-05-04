# Send mails

Script for sending custom emails to a maillist

## Getting Started

Instructions to get the project up and running

### Prerequisites

You will need [docker](https://docs.docker.com/install/) for this project.

### Installing

Build your docker image

```
docker build -t <tag-name> .
```

### Setup your e-mail

1. Make a copy of `maillist_example.csv`:

```sh
cp maillist_example.csv maillist.csv
```

2. Add your recipients and your messages to the `maillist.csv` file that was created.

3. Create a file named `mail.txt` and add your e-mail to it.

4. Create a file named `pw.txt` and add your password to it.

### Run your script

Run your script.
```
sudo docker run -it <tag-name> python send_mail.py
```

Use -v flag if you are editing the script and running. So you don't need to rebuild your container everytime.

```
sudo docker run -it [-v $PWD:/code] <tag-name> python send_mail.py
```

## Contributing

Feel free to use, contribute and send a PR. There is no contributing file to help you so far.

## Authors

Bruna Moreira

See list of contributors in this repo.

## License

This project is licensed under the GPLv3 - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Template for email [Email HTML io](emailhtml.io)
* Template for email [ohsik](https://github.com/ohsik/Simple-Responsive-HTML-Email-Template)
* [SMTPlib](https://docs.python.org/3/library/smtplib.html)
* [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* [email.mime](https://docs.python.org/3/library/email.mime.html)
* [csv](https://docs.python.org/3/library/csv.html)

