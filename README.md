import numpy as np
from PIL import Image
import matplotlib.pyplot as plt
#create butterfly imaage
butterfly=np.zeros((100,100,3))
#wings with patterns:
butterfly[20:40,30:70]=[1,0,0] red
butterfly[25:35,40:60]=[1,1,1] white spots
butterfly[20:40,70:90]={0,0,1] blue
butterfly[25:30,75:85]=[1,1,1] white spots
butterfly[60:80,30:70]=[0,1,0] green
butterfly[65:75,40:60]=[0,0,0] black lines
butterfly[60:80,70:90]=[1,1,0] yellow
butterfly[65:70,75:85]=[0,0,0] black lines
#body:
butterfly[40:60,50]=[0,0,0] black
#Antennae:
butterfly[30:40,85:95]=[0,0,0] left antennae
butterfly[30:33,85:95]=[1.1.1] left antennae white base
butterfly[60:70,85:95]=[0,0,0] right antennae
butterfly[67:70,85:95]=[1,1,1] right antennae white base
# Add pattern to antennaes:
for i range(30,40):
if i %2==0:
butterfly[i,89]=[1,1,1]
for i range(30,40):
if i % 2 ==0:
butterfly[i,86]=[1,1,1]
color_map=
[1,0,0]:1,#Red
[0,0,1]:2,#Blue
[0,1,0]:3,#Green
[1,1,0]:4,#Yellow
[0,0,0]:5,#Black
[1,1,1]:6,#White
#Create image:
img=Image.fromarray(butterfly.astype('uint8'),RGB)
img.save('butterfly.png')
#Display image:
plt.imshow(butterfly)
plt.axis('off')
plt.show()
#Robot class
class Robot:
def_init_(self,name):
self.name=name
self.x=0
self.y=0
def move_left(self):
self.x-=1
def move_right(self):
self.x+=1
def move_up(self):
def move_down(self):
self.y+=1
def read_code(self,code):
for line in code.split("\n"):
if line =="left":
self.move_left()
elif line == "right":
self.move_right()
elif line =="up":
self.move_up()
elif line =="down":
self.move_down()
#Create robot
robot=Robot("R1")
#Sample code
code="""
up
up
right
right
down
"""
import java.util.HashMap;
import java.util.UUID
public class DRM {
private Hashmap<String>licenses=
new Hashmap<>();
public boolean verifyLicense(String licenseKey){
if(!licenses.contairsKey(licenseKey))
return false,
String machineId=getMachineId();
returnlicenses.get(licenseKey).equals(machineId)
private String gerateLicense(StringmmachineId)
//Use some hardware info to generate
//a Uhique machineID
ruturn UUID.random UUID().toString();
public String licenseKey=UUID.random UUID()toString();
licenses.put(licenseKey,machineId);
return licenseKey;
public class Licensemanager
private String licenseKey,
public boolean is Licensed()
//check if license key is valid
return verify License(licenseKey);
private boolean verify License(licenseKey)
//Logic to verify license key
//E.g.Check against data base,decrypt,ect.
return true,
public void set LicenseKey(String Key)
licenseKey=Key;
import java.util.Random,
public class LicenseKey
private String generate Key()
String Key=
Random rand=new Random()
for(int i=0;i<8,i++)
int n=rand.nextInt(10)
Key+=Integer.toString(n)
Keys=Array Utils.add(Keys,Key)
return Key;
public boolean validateKey(String Key)
for(String K:Keys)
if(K.equals(Key)
return true;
}
}
return false;
}
}
//Usage
LicenseKey lic=new licenseKey()
string new Key=lic.generate Key()
if(lic.validate Key("abcd123"))
//allow access
}else
//deny access
