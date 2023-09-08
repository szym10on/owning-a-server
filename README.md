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
