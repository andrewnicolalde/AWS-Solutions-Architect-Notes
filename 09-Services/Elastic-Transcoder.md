# What is Elastic Transcoder

Elastic transcoder is a video transcoding service provided by AWS designed to transcode video into different formats best suited for a variety of devices and applications. For example, transcoding traget presets exist for Android devices, iPhones (including different models if iPhones), and even gifs! (See attached).

* Billing is based on the number of minutes of video transcoded as well as the resolution(?) TODO: Rseolution of output? Input? Both? Minutes of input or output or both??
* Incoming videos are ingested from an origin S3 bucket, transcoded and deposited in a target S3 bucket.
* I've been told (by Leo) that Elastic Transcoder is a legacy service now, having been replaced by Elemental MediaConvert.