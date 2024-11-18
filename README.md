# Odoo Tagged Order - Sync (Google Sheet)

## Sync custom tagged products orders to google sheeet

### Requirements:

- Python
- Odoo v16^
- PostresSQL Database

### Install Python and the required modules

```bash
sudo apt install python3 python3-pip
pip install -r requirements.txt
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
