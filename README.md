<h1 align="center">Automated Certificate Generator 📜</h1>
<h2 align="center">version-1.0.0</h2>
This repo contains my 2nd mini project that i've done while learning open CV and PILLOW modules in python.

Idea for this project striked me when i attended an online webinar hosted for more than 500+ participants for skill development,
at the end of the webinar everyone is awarded with a participation certificate. I wondered how did they managed to create 500+ certificates in less than an hr.
When i was learning open CV i came to know it can be easily implemented with built-in functions in cv module, but the problem is Open CV offers very little amount of fonts
there is no option to import o use other fonts.\
### In OpenCV, we have the following 8 fonts available,
-> Hershey Simplex\
-> Hershey Plain\
-> Hershey Duplex\
-> Hershey Complex\
-> Hershey Triplex\
-> Hershey Complex Small\
-> Hershey Script Simplex\
-> Hershey Script Complex

So i started to think of an alternative then i remembered PILLOW module , in which any font can be used regardlessly
Here i used <b>Pacifio</b> and <b>Sofia-regular</b> , u can find many fonts and can download for free from <a href='https://www.fontsquirrel.com/fonts/list/popular'>Fontsquirrel</a>

I made script which uses both Open CV and Pillow, user can choose between any of them by commenting the other in main function

```python
if __name__=="__main__":
    clean()
    name_ls=open_textfile()
    pillow(name_ls)
    cv_2(name_ls)
```
## note: certificates made using Open cv are stored inside cv2 dir, same applies for PILLOW

# Demo:
Intially if there are any certificates in pillow or cv2 dir are cleared/deleted then updated with new certificates, u can see the log of which certificate is generated in terminal (ik resolution is f'ed up)
<p align="center"><img src="preview.gif" align="center"></p>

### clean() demo:
```python
def clean():
       print("Cleaining........")
       for certificates in os.listdir("result/pillow/"):
        os.remove("result/pillow/{}".format(certificates))
       print("done........")
```
Just in case u forgot to delete previous certificates, clean is used to remove any previous remains. <b>open_textfile()</b> is used to read data from names.txt (don't forget to update names.txt with you're data before running script)

There is a small problem i couldn't rectify...

U have to manually change the x in "result/x/" and "result/x/{}" with pillow if u want to clear certificates in pillow dir, same applies for cv2. ( listdir() in OS module is not supporting ".format" technique for /<folder-name> ,or i don't know how to use it properly)
<hr style="border:10px solid grey"> </hr>

## That begin here is a quick sample created using Open CV and Pillow with Pacifico and FONT_HERSHEY_SCRIPT_COMPLEX fonts
<p align="center"><img src="preview-1.jpg" align="center"></p>
<p align="center">(found this beautiful certificate template in <a href='https://www.canva.com/design/play?type=TACTmE1fsnQ&template=EAExdwsjPiw&category=tACZCk6N0I4&schema=web-2&locale=en'>Canva</a>)</p>

### In either techniques u can adjust font-weight,thickness,font-size,font-color by changing values in their respective arguments

# Note:
--> As of now (1.0.0) input can only given by .txt file format, tried using pandas and xlrd for reading .csv nd .xlsx files but it didn't work out as intended.\
--> No other issues, everything works fine\
--> place you're template certificate with name strictly "certificate.jpg", update the co-ordinates for text placement, update names.txt -- # hit run and chillax! 
### --> Under GPL-3.0 license you are eligible to use the code how ever you want, but do not copy paste this as you're work/project anywhere , if done so it leads to copyright violation,you can avoid it by giving credit to me by linking this repo.

(ngl open CV, Pillow are dope af🔥!)
