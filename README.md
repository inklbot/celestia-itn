# Overview
#### This guide provides two methods for running PayForBlob Transactions.<br/><br/>
[Method_1 - CLI](https://github.com/inklbot/celestia-ITN-PayForBlob-Transactions/blob/main/README.md#method_1-guide)<br/>
[Method_2 - UI](https://github.com/inklbot/celestia-ITN-PayForBlob-Transactions/blob/main/README.md#method_2-guide)<br/>
<br/>
## Method_1 guide

#### Enter this command on the server running Celestia-node.
```
wget https://raw.githubusercontent.com/inklbot/celestia-itn/main/blob.sh && sed -i 's/\r//' blob.sh && chmod +x blob.sh && sudo /bin/bash blob.sh
```

## Method_1 Example
#### Run `blob.sh`
<img width="80%" src="https://user-images.githubusercontent.com/31788091/229029309-50a1ebe6-e55f-48b1-bd72-9a78e5e17105.PNG"/>
<br/>
<img width="80%" src="https://user-images.githubusercontent.com/31788091/229029310-a5a5c3fd-b1a5-4929-9fe3-b54222ece5ed.PNG"/>
<br/>
<img width="80%" src="https://user-images.githubusercontent.com/31788091/229029313-0e3e49d5-fdf1-4785-8f57-e1d0e5b20a7f.PNG"/>
<br/> When you ran the `blob.sh`
<br/><br/>
<img width="80%" src="https://user-images.githubusercontent.com/31788091/229029315-89ebb6d7-80ac-476e-a80a-90ab3454d562.PNG"/>
<br/>Go through the attached mintscan link and check if the TxHash, Height, and Wallet address are correct
<br/>
<br/><br/>
<img width="80%" src="https://user-images.githubusercontent.com/31788091/229029324-ac465602-c946-4425-9678-b712f963ccb4.PNG"/>
<br/>Go to tiascan and check the PayForBlob Count.

## Method_2 guide

Install `screen, python3, pip` and install `flask` module

```
sudo apt install screen python3 python3-pip -y
pip install flask
```
<br/>
Download `web_server.py`
```
wget https://raw.githubusercontent.com/inklbot/celestia-ITN-PayForBlob-Transactions/main/web_server.py
```
Create `dashboard` folder and download index.html
```
mkdir dashboard
cd dashboard
wget https://raw.githubusercontent.com/inklbot/celestia-ITN-PayForBlob-Transactions/main/index.html
```
Split terminal using screen
```
screen -S web_server
```
Run `web_server.py` in a split terminal
```
python3 web_server.py
```

## Method_2 Example
