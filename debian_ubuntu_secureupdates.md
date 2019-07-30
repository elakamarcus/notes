# Secure updates
This is to enable support for secure updates\
Note: This is usually not necessary for e.g. ubuntu provided repositories that use other means of ensuring the packages you get are the ones you should get etc. See more information [Here](https://askubuntu.com/questions/352952/are-repository-lists-secure-is-there-an-https-version)

## Procedure

### fetch the required additional packages

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https
```

### updates sources list

Now update the URLs for apt to fetch, so they point to the https-version:
Note:```[control-r]``` this is a button combination, of control and r pressed together.

```$ sudo nano /etc/apt/sources.list```\
[control-w] //to enter search\
```Search:  ```\
[control-r] //tell nano to replace\
```Search (to replace): ``` **http:**\
```Replace with:  ``` **https:**\
Now press enter, and you can either inspect and press enter for each occurence, or type ```a``` to replace all.
When you're done, press [control-o] to write to file, and then [control-x] to exit.

### test to verify

Now just do ```sudo apt update``` to make sure it is working.

Enjoy
