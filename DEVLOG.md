### 04/06/2021
I'm about to go on a ~1.5 mile run-jog, target is below: (using Daft Logic's distance calculator)

![distance calculated of run](./run.JPG)

Anyway I was motivated to do this because the app I used to use was acquired by some company and I was like okay fine, can I just buy it once. No it's either free with ads or you pay a subscription. Like nah chief.

So yeah I'm going to make a piece of crap one... anyway more exposure to imu related.

It seems like all the stuff I want (GPS, IMU) are accesible even directly by web, so I will make a stupid interface/host it on GPages and run/gather some data. I can't do any processing now but my concern is storing data against localStorage for the time that I run. Despite one lap being 0.7 miles, after I sprint the road part (bottom to top) then I'm pretty much sucking wind... till I get to the next straight away, run half of it... sucking wind... then I sprint up the hill which is nice. Then I feel my lungs burn, like they were being deep fried with some panko.

This will become an RN app as I have to deploy some.

![basic interface](./basic-interface.JPG)

Two buttons, start/stop and then live data stream to make sure it's working and then old data when I stop/start, see they're being stored.

A concern is how much data I can store, I think 1 second at a time is not bad... maybe 2 seconds. But yeah I think my limit is 2.5MB and not sure with the length of the floats how much each row will take up.

 Right now I weigh 260lbs insane... normally I'm in the 220's, ideal is 205-215. I'm super cut in the low 200's.

 Working at home for so long like I haven't had to fit in my own clothes or anything except for the biggest ones.

 Going to kick off this github pages... gotta get this prototype done in like 50 mins or less so I can have some daylight left to actually run.

 My fear is it will stop working/not collect data.

 How it works is every say 100 seconds it will push a group into the localStorage so that I don't have to worry about the variables getting too big/accidentally losing data.

 I'll have to piece the data together later.

 Oh I need a way to export this data though hmm...

 Maybe I can add the UI update later and pull it from localStorage still

 Ahh I don't know what to make of these different sensors looks like some take out gravity for example, some combine... also this ticking thing vs. on demand (what I wanted)

 Crap I'm out of time, need to just get location data

 Ugh I'm out of time, running is what matters, I gotta get out there

 ![it ain't much meme](./sucks.JPG)

 Gotta turn on the Omni-man song where he murders the Flaxan planet

### return from "running"

 Well that was a failure

 I had a couple of dumb things happen like I'd switch to my music player and I would lose all data(the web tab would disappear). Or I would try to scroll down but I didn't have overflow in so I would accidentally refresh the entire page... ahh. But I did get some samples, some learning points.

 Like I think 2 seconds is too much sampling for the speed I'm moving.

 Also I guess it does not take that much time for me to do my stuff. Two laps is about 30 minutes, I'm spending most of my time walking currently because the arches of my feet are on fire from the hill/divots in the ground.

 Still this is cool, developing something I want to use and need to do "defensive coding" due to not being able to change anything at the field.

 I still have to gather samples of each acceleration type, I'll probably do testing indoors first.

 Shots of the hill

![entrance](./hill.png)

![looking at entrance](./from-the-end.JPG)

It is a nice little area see the lake

![the lake](./lake.JPG)

The actual data

![2 minute sample](./2-minutes.JPG)

Another one

![another data sample](./another.JPG)

wtf these coordinates don't match oh no...

39.1501877,-94.7898527 (correct)
39.2151788,-94.7563776 (what I measured)

I don't understand this how is it so bad, GPS apps have it almost perfect... hmm wonder if it it's the tower

geolocationl.watchPosition sounds good vs. calling/invoking everytime

maybe [this](https://stackoverflow.com/questions/16202077/high-accuracy-geolocation-html5), anyway I'm super burnt, will put more time into this