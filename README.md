# Odoo Loyalty Program - Extender

## Sync Loyalty Programs from multiple Odoo instances using the unique customer's barcode

### Requirements:

- Python
- Odoo v16
- PostresSQL Database

### Notes:

You must configure Odoo to enable the `"Discounts, Loyalty & Gift Card"`.

Configure customer to have a unique `barcode` as it is used to identify unique customers.

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

- `tag_id` - <b>Important!</b> The tag id for product that will be sync
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
```

### Display help information

```bash
python3 listener.py -h
# or
python3 listener.py --help
```

#### by [mikee](https://github.com/mikesaraus)@[accountador.com](https://accountador.com)
