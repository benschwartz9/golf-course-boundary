# jd_golf


### Install from requirements.txt
pip install -r requirements.txt



### Data Grab (manual): Method 1
Go to https://code.earthengine.google.com/
    - Paste codeearth_rbg.js in the code editor (middle box) and run  -> allows you to see the satellite view of the golf courses
    - Draw a bounding box around one/both of the golf courses and name it "myregion"
    - Paste codeearth_extract.js in the code editor in run
    - This saves a series of .tif files to your Google Drive
Download .tif files from your Google Drive to your local machine
Run tif2jpg.py on each .tif file to convert to jpg
Stitch together jpg files using stitch_images.py to 1 final image
    - code edits in stitch_images.py will probably be needed

### Data Grab (API): Method 2
Make sure you have "pip install earthengine-api"
Run "earthengine authenticate" to authenticate session with Google Account
Run download_image.py to download .tif file
    - This process saves each band over the same area as a separate .tif file (area.R.tif = red, area.B.tif = blue)
Use multitif2jpg.py to convert to JPG