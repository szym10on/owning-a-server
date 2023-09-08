# Build, configure, manage and secure your (Minecraft) or other server

[?] In this project I will grant information about how I independently built, configured, managed and secured my physical server

---

## History of my server

xyz

---

## Building a server PC and searching for best hardware

**Selecting the right components for a Minecraft server PC is crucial for delivering a smooth and enjoyable gaming experience to players. Here's why it's essential to pick the best parts and prioritize a CPU with high GHz and ample RAM**

1. The most important part of our build will be our CPU:

- Minecraft servers require real-time processing power to handle player interactions, world generation, various game mechanics, plugins and scripts. A powerful CPU with a high clock speed (GHz) ensures that the server can respond quickly to player actions, minimizing lag and delays. Before buying one from the internet I was reserching a lot of the internet. One of the best things you should look for are older CPUs with high clock speed that needs a cheap motherboard if you have low budget. But if you have unlimited money to spend on your server PC you can get one of the newest AMD Ryzen CPU and that should work perfectly.

- If you are looking for a budget build you need around $150 for CPU for a smooth server experience. Here are best CPUs for every price range:

Intel CPUs with high clock speed:<br>
➤ i9-11900K ($400-$500)<br>
➤ i7-11700K ($300-$400)<br>
➤ i5-11600K ($200-$300)<br>
➤ i3-10100 ($100-$150)

AMD CPUs with high clock speed:<br>
➤ Ryzen 9 7950X ($550-$650)<br>
➤ Ryzen 9 5900X ($350-$450)<br>
➤ Ryzen 7 5800X ($200-$300)<br>
➤ Ryzen 5 5600X ($100-$150)

- CPUs in a price range of $100-$300 should work fine with servers for 5-30 players if the server is well optimized. For a larger servers you should look for a better CPU in a price range of $300+ and don't forget to include RAM, SSD, motherboard and computer power supply costs.

2. Second most important thing for our server will be RAM:

- Minecraft server require a lot of RAM if you are looking to hold more than 5 players and load a lot of chunks for your server. You can lower that amount by using some kind of unloading chunks plugins that will unload unused chunks after player leaves them. That will grant you more free memory to work with.

- Let's talk numbers that are always diferent if you will look for them on other forums. As someone that worked with servers and I draw big attention to performance. Here are a little calculation you can do when you are looking for best RAM usage:

- (max players * 100) + ((plugins + scripts) * 50) + (world size in GB * 50) = RAM in MBs<br>

You should always round up. If your are looking for a server with 20 players, 50 scripts and a world size of 30GB you will do: (20 * 100) + (50 * 50) + (30 * 50) = 6000MB, 6000MB = ~6GB of RAM so you should buy 8GB RAM if you are looking to be safe.

3. Last but not least is our memory disk:

- When you are looking for your Minecraft server memory disk you should always look for a fast write and read disk. If you can afford M.2 disk you should look for one but any other SATA SSD disk should work fine. Always check the storage size and don't let your files override more than 75% of the size because it can cause lags and falsly saved files.

4. In addition:

- You can buy yourself a power supply that consume little electricity and a good case that circulatates for better temperatures.

- The cost of running your server 24/7 depends on your power supply, usage and electricity costs in your area. On average my server cost me about $5 per month.

---

## Selecting best OS for your server PC

**There are a lot of operating systems for hosting server like that but I will keep it simple.**

1. I always used the defualt Ubuntu Server w/o graphical UI and it worked perfectly fine all the time.

- Instalation of Ubuntu Server is really simple. If you need help just search how to install Ubuntu Server on your PC on youtube.

2. Important commands for your server and how to use Ubuntu:

➤ File System Commands:<br>
ls: List files and directories in the current directory.<br>
cd: Change the current directory.<br>
pwd: Print the current working directory.<br>
touch: Create an empty file.<br>
mkdir: Create a new directory.<br>
cp: Copy files or directories.<br>
mv: Move or rename files or directories.<br>
rm: Remove files or directories.<br>
cat: Display the contents of a file.<br>
more or less: Display the contents of a file one screen at a time.<br>
nano or vim: Text editors for editing files in the terminal.<br>

➤ System Information:<br>
uname: Display system information.<br>
top or htop: Monitor system resource usage.<br>
df: Display disk space usage.<br>
free: Display system memory usage.<br>
lscpu: Display CPU information.<br>

➤ User and Permissions:<br>
whoami: Show the current user.<br>
passwd: Change user password.<br>
sudo: Execute commands with superuser (administrative) privileges.<br>
chown: Change file or directory ownership.<br>
chmod: Change file or directory permissions.<br>

➤ Package Management:<br>
apt-get or apt: Package manager for installing, updating, and managing software packages.<br>
dpkg: Package manager for handling individual package files.<br>
snap: Package manager for installing snaps (containerized applications).<br>

➤ Networking:<br>
ifconfig or ip: Display network interface information.<br>
ping: Send ICMP echo requests to test network connectivity.<br>
ssh: Securely connect to remote servers.<br>
wget or curl: Download files from the internet.<br>
netstat or ss: Display network statistics.<br>
traceroute: Trace the route packets take to reach a host.<br>

➤ Process Management:<br>
ps: List running processes.<br>
kill or killall: Terminate processes.<br>
bg and fg: Manage background and foreground processes.<br>

➤ Archiving and Compression:<br>
tar: Create and extract tar archives.<br>
gzip, bzip2, xz: Compress and decompress files.<br>

➤ File Searching and Manipulation:<br>
find: Search for files and directories.<br>
grep: Search for patterns in text files.<br>
locate: Quickly find files based on a database.<br>

➤ File Transfer:<br>
scp: Securely copy files between hosts.<br>
rsync: Synchronize files and directories between systems.<br>

➤ Text Processing:<br>
sed: Stream editor for text manipulation.<br>
awk: Text processing tool for data extraction and reporting.<br>

➤ Shell Scripting:<br>
bash or other shells: Run shell scripts and command-line automation.<br>

➤ System Administration:<br>
systemctl: Control and manage systemd services.<br>
journalctl: View system logs.<br>
ufw: Uncomplicated Firewall for managing firewall rules.<br>

---

## Setting up your server for public network

**This is probably the hardest part of building your network. In most cases you have to pay for a fixed IP address. To do that you have to contant your ISP (Internet Service Provider) and ask for static public IP address for your network. In my case it was about $5/month of cost for that type of IP address**

1. Set up a static IP address for your server PC (in Ubuntu Server w/o graphical view):

- Check your interface name by typing 'ip a'

![1](https://github.com/szym10on/owning-a-server/assets/123908381/1290fff9-c703-4f4c-bca8-0faa7bea73cc)<br>
Network name is in red circle. Write it down or copy the name of it.

- Edit the network configuration file by typing 'cd /etc/netplan/' than type 'ls' to list file in that directory

![2](https://github.com/szym10on/owning-a-server/assets/123908381/a177b88f-37a5-4b0b-a178-b76e6afbc91e)<br>
The .yaml file should pop out.

- Edit that file with 'sudo nano "file name"'

![3](https://github.com/szym10on/owning-a-server/assets/123908381/ef550258-0ef9-467b-8ec7-0ba7e0755079)<br>
Edit the file as shown. Don't forget the number of spaces before every line.<br>
Replace <interface> with your interface name like "eth0" or other name that you check before.<br>
Set dhcp to "no". Set your desired static IP address and remember it. Set your gateway address to your router address.<br>
If you encounter a problem you can always look for more advanced tutorial on how to set it up.

- After editing network file use Ctrl + O than Enter, next press Ctrl + X to exit out of nano editor.

- To set all the things that we edited use 'sudo netplan apply' and 'sudo systemctl restart network-manager' to restart your network.

2. Set up port forwarding in your network router:

- Log in to your router. Common router IP addresses include 192.168.0.1 or 192.168.1.1. Consult your router's manual or documentation for the correct IP address and login credentials

- Locate the port forwarding section in your router settings. This may be called "Port Forwarding," "Port Mapping," or something similar, depending on your router's brand and model.<br>
Add a port forwarding rule for the Minecraft server. Specify the following information:<br>
➤ External Port: The port number you want to use for incoming connections (e.g., 25565 for default Minecraft).<br>
➤ Internal IP Address: The static internal IP address of your Minecraft server that you set up earlier in .yaml file of your server<br>
➤ Internal Port: The same port number as the external port (e.g., 25565).<br>
➤ Protocol: Select "TCP".

- Save configuration and restart your router.

- Check your public IP by searching 'what is my ip' in your browser. Well done - that's your server public IP!

