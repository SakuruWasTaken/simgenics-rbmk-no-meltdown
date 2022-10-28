# simgenics-rbmk-no-meltdown
<img src="https://cdn.discordapp.com/attachments/832540923278786600/1035374960681693236/aaaa.PNG">
This is a modified version of itchy-avacado's improved version of the Simgenics RBMK simulator, the only difference is it won't terminate the simulation if you go above 100% neutron flux.

# How to run
You can download the files [here](https://github.com/SakuruWasTaken/simgenics-rbmk-no-meltdown/archive/refs/heads/main.zip)

Then extract them into a folder.

Then open the folder named "Chernobyl Reactor Simulator" and run RXMODEL.exe

# How I made this
First, you need to open RXMODEL.exe in dnspy (which you can download [here](https://github.com/dnSpy/dnSpy/releases/tag/v6.1.8), then navigate to the class "model_timer", then do ctrl+f and search "meltdown"

Now, you will see a line that says flag3 = (flx > 1f);  right click on it, and click "Edit IL Instructions"
You need to change the value "1" to something higher, for instance 1 = 100%, 2 = 200% and so on, i just set it to 999, but you can set it to anything you want.

Once you've changed the value, click OK, then go to File, then Save Module, then set the path to whatever you want, then click OK.

Now open the simulator with the executable you saved.
