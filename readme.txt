Using 3.1.4

1. after cloning, create a subfolder in this repo called "custom_files_wmata"
2. In that folder, place a pbf file downloaded from mapzen. Ideally, you will also have downloaded the entire US South and then clipped to the appropriate area.
3. open command prompt/powershell, cd into the repo, and type 
docker-compose up
This is how you will start the valhalla instance each time.
4. WAIT. it will take a while to do its thing. this will be muhc much faster the next time around but the first go around it will download the docker image.
5. When you see "Found config file. Starting valhalla service!" you can start sending api requests.

For WMATA, using the following bounds based on the bounding box of its buzzones

osmosis --read-pbf us-south-latest.osm.pbf --bounding-box left=-77.48609 bottom=38.57621 right=-76.61750 top=39.23154 --write-pbf wmatabuzzonebbox_20220322.pbf

