# nsfwproxy

## NSFW-detecting proxy based on Caffe, OpenNSFW and Proxy2

This is a proof of concept implementing NSFW detection on a proxy, using a convolutional network trained with Yahoo open sourced openNSFW

Please do NOT use this is production, although it performs very well on lab scale it's not meant to be used on production.

The script detects any NSFW image and send a 403 error to clients wherever the threshold exceeds 0.2 (adjustable)

Usage:


`python proxy2.py --model_def PATH_TO_PROTOTXT --pretrained_model PATH_TO_CAFFEMODEL`

Example

`python proxy2.py --model_def /home/open_nsfw/nsfw_model/deploy.prototxt  --pretrained_model /home/open_nsfw/nsfw_model/resnet_50_1by2_nsfw.caffemodel`
 
 You can get opennsfw from [here](https://github.com/yahoo/open_nsfw) and caffe from [here](http://caffe.berkeleyvision.org/).
 
Base code for the proxy [here](https://github.com/inaz2/proxy2) 
