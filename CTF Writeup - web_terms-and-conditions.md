The challenge: 

![Screenshot 2024-02-22 at 11.25.43 PM.png](../_resources/Screenshot%202024-02-22%20at%2011.25.43 PM.png)

What happens when you open the page: 

![Screenshot 2024-02-22 at 11.30.00 PM.png](../_resources/Screenshot%202024-02-22%20at%2011.30.00 PM.png)

This is my first time participating in any CTF, so I was really just playing around and seeing how much I could solve with not really any experience (and maybe learn some new things along the way!) I tried to click on the "I accept" button but 

![Screenshot 2024-02-23 at 12.13.41 PM.png](../_resources/Screenshot%202024-02-23%20at%2012.13.41 PM.png)

Which made sense because obviously it wouldn't be THAT easy... The next (and pretty much only) idea I had was to try playing around with inspect element, but this showed up the moment I opened it: 

![Screenshot 2024-02-23 at 9.39.31 PM.png](../_resources/Screenshot%202024-02-23%20at%209.39.31 PM.png)

I wasn't really sure where to go from here --- looking at just the HTML on this screen, I couldn't find any useful information. I clicked around on the different tabs, but nothing seemed to be helpful. Somehow during my random clicking I had the amazing idea of reloading the page

![Screenshot 2024-02-23 at 10.12.55 PM.png](../_resources/Screenshot%202024-02-23%20at%2010.12.55 PM.png)

Which magically fixed the problem, and the text and button showed up normally again (now playing around with the page after the contest, I've realized that it triggers "no console allowed" whenever the window size changes, but I didn't know that at the time). Continuing with my initial idea, I wanted to remove the script code that controls the movement of the button based on the cursor position. This was a bit tricky because I did not know how to work with inspect element at all, but I found a way to edit the code through the "Sources" tab. I initially wasn't able to directly remove the code block, but I found an option called "Override content"

![Screenshot 2024-02-24 at 2.41.41 AM.png](../_resources/Screenshot%202024-02-24%20at%202.41.41 AM.png)

After selecting a folder (and getting a silly warning about granting access and making sure to not expose any sensitive information), I was able to remove the setInterval() code which effectively stopped the button from moving around, but I clicked the button and this happened...

![Screenshot 2024-02-24 at 8.10.43 PM.png](../_resources/Screenshot%202024-02-24%20at%208.10.43 PM.png)

So now I'm back at square one and have no ideas on how to click the button without just disabling the code. Lucky for me though, after clicking around some more I found a tab called "Event Listeners."

![Screenshot 2024-02-24 at 8.14.00 PM.png](../_resources/Screenshot%202024-02-24%20at%208.14.00 PM.png)

I tried removing this, and was able to click the button and get the flag!

![Screenshot 2024-02-24 at 8.16.55 PM.png](../_resources/Screenshot%202024-02-24%20at%208.16.55 PM.png)

Side note: Before I was able to go on my computer, I actually initially accessed the challenge webpage through my phone and saw this: 

![28B6E180-989C-4DA0-B560-8877C454A1C6_1_201_a.jpeg](../_resources/28B6E180-989C-4DA0-B560-8877C454A1C6_1_201_a.jpeg)

And it makes sense that this exists --- or else it would probably be too easy to solve by just pressing the button on a touchscreen device. 

Overall, I think I learned a lot just by playing around and doing some google searching to see what I could do in inspect element, and it was super rewarding to solve my first non-trivial challenge!