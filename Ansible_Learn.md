
# Adhoc Commands 

1) free -m
2) uptime 
3) ansible web_group[group of Inventory] -m ping[ module name]
4) ansible web_group -m shell -a 'free -m'
5) ansible web_group -m shell -a 'uptime'
6) ansible web_group -m shell -a 'yum list installed | grep nginx'
7) ansible webgroup -m sheel -a 'yum list installed | grep perl'
8) ansible-doc -l [list modules] 
9) ansible [group] -m copy -a [src=source_path dest=destination_path]  --> copy file on ansible clients from ansible controller
10) ansible [group] -m copy -a [content=" File content Here" dest="destination_path"] --> complete filename , path has to be defined.

# Ansible creates .py file that eventually runs on the client machine. 

# User can create Files or Directories on Ansible clients from Ansible Controller using File Module.
1) ansible [group] -m file -a "path=file/dir destination location state=<State>"
2) 
  
  
  
  
  

