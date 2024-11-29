# ComputerNetwork_Assignment1
## Requirement
```bash
python >= 3.7
```
## Installation

```bash
pip install bencode.py
```
## Description
### tracker.py
This file contain class tracker which is represented to tranfer information to peer
### peer.py
Upload torrent file or download file using a metainfo torrent
### utils.py 
This file contain functions which is using to manage file metainfo , pieces and  folder.



## Command line interface
### tracker.py
```bash
python tracker.py --ip your_ip --port your_port --metainfo-storage your_folder_metainfo --header-length bytes
```
python3 tracker.py --ip 10.0.188.213 --port 5050 --metainfo-storage metainfo --header-length 1024

### peer.py
```bash

python peer.py --ip your_ip --port your_port --tracker-ip your_tracker_ip --tracker-port your_tracker_port  --header-length bytes\
--metainfo-storage your_folder_metainfo\
--pieces-storage your_folder_hold_pieces\
--ouput-storage your_folder_output\
--download file1.torrent file2.torrent ....
--become-seeder\   # upload after complete download
--upload input1.mp4 input2.pdf ....
```

python3 peer.py --ip 10.0.188.213 --port 4042 --tracker-ip 10.0.188.213 --tracker-port 5050  --header-length 1024 --metainfo-storage metainfo2 --pieces-storage pieces2 --output-storage output2 --download metainfo/Lab3_Inclass_L13_2213781.torrent