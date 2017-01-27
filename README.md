# Hunter. This code is written on Python 2.7.13 with the following libs installed: 
# pcapng (https://pypi.python.org/pypi/python-pcapng)
# arp_table (http://python-arptable.readthedocs.io/en/latest/readme.html). 

# The goal of the program is to seek out pairs of MAC addresses from the ARP table and logs from network sniffing tools (in pcap format).
# When a pair is found, it is disgarded. We are only looking for mismatched MAC addresses to find potentially harmful systems

# I trust you'll be able to install the necessary modules on your own provided you follow the documentation/instructions
# as listed on the above pages.

# From the python_arptable (arp_table) module we will import we will only import the 'get_arp_table()' fuction as that will provide us
# with the most recent version of the ARP Table entries. This fuction can be used even without running this script if you need to
# reference previous tables, but for sake of ease, we will only reference our most recent ARP cache and network traffic.

# This script will need to reference a *.pcapng* file type based on the location of the file. For this, if you do not have it installed
# already, I suggest you install the most recent version of WireShark and become with it's functionalities. Other alternatives include
# nfdump, save you can output your results to a pcap file. I chose not to take this route since my familiarity with command line is in its
# infancy but if you wish, please feel free to email me @ y1966.steve @ gmail . com and provide some feedback. You will need the direct
# file path in order to produce a result.

# The syntax is as follows: 

# python hunter.py /home/.../****.pcapng
# with the asterisks being the name you saved the file as.
