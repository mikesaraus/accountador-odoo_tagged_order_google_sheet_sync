# Odoo Tagged Order - Sync (Google Sheet)

## Sync custom tagged products orders to google sheeet

### Requirements:

- Python
- Odoo v16^
- PostresSQL Database

### Install Python and the required modules

```bash
# Python
sudo apt install python3
# Pip
sudo apt install python3-pip

# Modules
# using pip
pip3 install -r requirements.txt
# or
pip3 install dotenv
pip3 install psycopg2
pip3 install requests
pip3 install google-api-python-client
pip3 install google-auth
pip3 install google-auth-oauthlib
pip3 install google-auth-httplib2
# or using apt package manager for system wide (service)
sudo apt install python3-dotenv python3-psycopg2 python3-requests python3-google-auth python3-google-auth-oauthlib python3-google-auth-httplib2
# install google-api-python-client for service
sudo pip3 install --break-system-packages google-api-python-client
```

### Configure `.env`

```bash
# copy .env.example to .env
cp .env.example .env
# then update the values accordingly
nano .env
```

### Important .env keys

- `tag_id` - <b>all db fallback tag id!</b> The tag id for product that will be sync
- `dbname` - the database name
- `dbuser` - the database user
- `dbpassword` - the database password of the user
- `dbhost` - the database host; default = localhost
- `dbport` - the database port; default = 5432

### Configure db.config.json

```bash
# copy db.config.sample.json to db.config.json
cp db.config.sample.json db.config.json
# then update the list accordingly
nano db.config.json
# Note: please specify the tag id
```

### Display help information

```bash
python3 listener.py -h
# or
python3 listener.py --help
```

#### by [mikee](https://github.com/mikesaraus)@[accountador.com](https://accountador.com)
