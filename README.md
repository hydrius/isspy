# ISSpy

## Introduction

This project began when I wanted to illuminate my lifx bulb when the International Space Station is less than five minutes away. Open Notify was the only library I could find to provide this information. However it was not completely accurate - at least at my location (Melbourne, Australia)<sup>1</sup>. 

<sup>1</sup> https://github.com/open-notify/Open-Notify-API/issues/20

## Installation

There is no backwards capability with python2. Please use python3 if you want to use this library. 

> pip install isspy

## Usage

For the moment, this library uses Spot The Station by default. Country, Region and City are given in the url for Spot the Station.
e.g https://spotthestation.nasa.gov/sightings/view.cfm?country=Australia&region=Victoria&city=Melbourne

    from isspy import isspy
  
    country = "Australia"
    region = "Victoria"
    city = "Melbourne"

    passes = isspy.ISSpy(country, region, city)

    #Returns list of passes as a dictionary
    print(passes.get_passes())

    #expected output
    [{'datetime': datetime.datetime(2019, 4, 20, 19, 14), 
      'duration': 1, 
      'elevation': 17, 
      'approach_elev': 11, 
      'approach_dir': 'N', 
      'departure_elev': 17,
      'departure_dir': 'NNE'}] 

## Future

Open-Notify also provides the current location of the ISS and the people aboard. I will incorporate this at a later date. 