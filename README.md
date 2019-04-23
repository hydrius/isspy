# ISSpy

## Introduction

This project began when I wanted to illuminate or flash my LED lightglobe when the International Space Station (ISS) was approaching. 

## Installation

There is no backwards capability with python2. Please use python3 if you want to use this library. 

> pip install isspy

## Usage

This library uses both Spot The Station & Open Notify. It uses Spot the Station for pass location by default. This is due to this bug https://spotthestation.nasa.gov/sightings/xml_files/Australia_Victoria_Melbourne.xml that seems to provide inaccurate information. However you can use Open Notify 

    country = "Australia"
    region = "Victoria"
    city = "Melbourne"

    passes = ISSNotify(country, region, city)

    #Returns list of passes as a dictionary
    print(x.get_passes())

    [{'datetime': datetime.datetime(2019, 4, 20, 19, 14), 'duration': 1, 'elevation': 17, 'approach_elev': 11, 'approach_dir': 'N', 'departure': 17, 'departure_dir': 'NNE'}] 