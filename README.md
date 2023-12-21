# lora_installer
1. Create a [Retool](https://retool.com/) account 

2. Create two databasaes via importing via .CSV 
3.  **install_log.csv**
4.  **joins_and_sends.csv**

5. Create two apps by selection import from JSON 
6.  **lora_installer.json**          -- Mobile app
7.  **lora_install_history.json**    -- Web dashbaord

## Database import
All field default to TEXT some need to be INT4 and TimnestampZ
![alt text](https://github.com/industrialinternet/lora_installer/blob/main/import_db_1.png "import")

### Import install_log CSV 

![alt text](https://github.com/industrialinternet/lora_installer/blob/main/install_log_import.png "import install log csv")

### Import joins and sends CSV

![alt text](https://github.com/industrialinternet/lora_installer/blob/main/joins_and_sends_1.png "import joins_and_sends csv")

### SQL update statement for setting joned and sent states 
UPDATE joins_and_sends SET status='joined', joined_at='2023-12-19 08:48:33.534660834' WHERE dev_eui='AABBCCDDEEFF0011';
UPDATE joins_and_sends SET status='sent', sent_at='2023-12-19 08:54:23.534660834' WHERE dev_eui='AABBCCDDEEFF0011';

