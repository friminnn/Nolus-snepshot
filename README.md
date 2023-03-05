# Nolus-snepshot

```
sudo systemctl stop nolusd
cp $HOME/.nolus/data/priv_validator_state.json $HOME/.nolus/priv_validator_state.json.backup
rm -rf $HOME/.nolus/data

wget http://93.81.241.55:8000/nolusdata.tar.gz 
tar -C $HOME/ -zxvf nolusdata.tar.gz --strip-components 1
mv $HOME/.nolus/priv_validator_state.json.backup $HOME/.nolus/data/priv_validator_state.json

sudo systemctl start nolusd && sudo journalctl -u nolusd -f --no-hostname -o cat
```
