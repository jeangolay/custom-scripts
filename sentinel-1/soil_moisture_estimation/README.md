# Soil Moisture Estimation Script

<a href="#" id='togglescript'>Show</a> script or [download](soil_moisture_estimation.js){:target="_blank"} it.
<div id='script_view' style="display:none">
{% highlight javascript %}
      {% include_relative soil_moisture_estimation.js %}
{% endhighlight %}
</div>

## Evaluate and visualize   
 - [Sentinel Playground Temporal](https://apps.sentinel-hub.com/sentinel-playground-temporal/?source=S1-AWS-IW-VVVH&lat=49.58263077421254&lng=-97.78971236664802&zoom=11&preset=CUSTOM&layers=VV,VV,VV&maxcc=20&gain=1.0&gamma=1.0&time=2017-01-01%7C2019-10-31&atmFilter=&showDates=false&evalscript=LyoKClN1cmZhY2UgU29pbCBNb2lzdHVyZSAoU1NNKSByZXRyaWV2YWwgdXNpbmcgY2hhbmdlIGRldGVjdGlvbiBhcHByb2FjaC4KCkF1dGhvciBEZXRhaWxzOiAKTmFyYXlhbmEgUmFvIEIuCjIwNi1NUlNMYWIsIENTUkUsCklJVCBCb21iYXksIEluZGlhLgoKQSBkZXRhaWxlZCBleHBsYW5hdGlvbiBvZiB0aGUgaW1wbGVtZW50ZWQgYWxnb3JpdGhtIGNhbiBiZSBmb3VuZCBpbiB0aGUgZm9sbG93aW5nIGFydGljbGVzLgoKV2FnbmVyLCBXLiwgTGVtb2luZSwgRy4sIEJvcmdlYXVkLCBNLiBhbmQgUm90dCwgSC4sIDE5OTkuIApBIHN0dWR5IG9mIHZlZ2V0YXRpb24gY292ZXIgZWZmZWN0cyBvbiBFUlMgc2NhdHRlcm9tZXRlciBkYXRhLiAKSUVFRSBUcmFuc2FjdGlvbnMgb24gR2Vvc2NpZW5jZSBhbmQgUmVtb3RlIFNlbnNpbmcsIDM3KDIpLCBwcC45MzgtOTQ4LgoKQi4gQmF1ZXItTWFyc2NoYWxsaW5nZXIgZXQgYWwuLCAKIlRvd2FyZCBHbG9iYWwgU29pbCBNb2lzdHVyZSBNb25pdG9yaW5nIFdpdGggU2VudGluZWwtMTogSGFybmVzc2luZyBBc3NldHMgYW5kIE92ZXJjb21pbmcgT2JzdGFjbGVzLCIgCmluIElFRUUgVHJhbnNhY3Rpb25zIG9uIEdlb3NjaWVuY2UgYW5kIFJlbW90ZSBTZW5zaW5nLCB2b2wuIDU3LCBuby4gMSwgcHAuIDUyMC01MzksIEphbi4gMjAxOS4KCiovCgpmdW5jdGlvbiAgc2V0dXAgKGRzcykgCiAgewogICAgc2V0SW5wdXRDb21wb25lbnRzKFtkc3MuVlYsZHNzLlZIXSk7IC8vIHNlbGVjdGluZyB0aGUgZGF0YXNldHMKICAgIHNldE91dHB1dENvbXBvbmVudENvdW50KDMpOyAvLyBGb3IgUkdCIG91dHB1dCBubyBvZiBjaGFubmVscyA9MwogIH0KZnVuY3Rpb24gZmlsdGVyU2NlbmVzIChzY2VuZXMsIGlucHV0TWV0YWRhdGEpIAogIHsKICAgIHJldHVybiBzY2VuZXMuZmlsdGVyKGZ1bmN0aW9uIChzY2VuZSkgewogICAgLy8gQ29uc2lkZXJpbmcgMzYgbW9udGhzIGRhdGEgdG8gYXZvaWQgc2Vhc29uYWwgdmFyaWF0aW9ucyBpbiBtYXNraW5nCiAgICByZXR1cm4gc2NlbmUuZGF0ZS5nZXRUaW1lKCk%2BPShpbnB1dE1ldGFkYXRhLnRvLmdldFRpbWUoKS0zNiozMCoyNCozNjAwKjEwMDApIDsgIC8vIERhdGEgZnJvbSAzNiBtb250aHMgdG8gY3VycmVudCBkYXRlCiAgICB9KTsKICB9CgpmdW5jdGlvbiBldmFsdWF0ZVBpeGVsKHNhbXBsZXMsIHNjZW5lcykgCiAgeyAgCiAgICB2YXIgY291bnQgPSAwOwogICAgdmFyIE12ID0gMDsKICAgIHZhciBtYXggPSAwOwogICAgdmFyIG1pbiA9Mi4wOwogICAgdmFyIHN1bV9WViA9IDA7CgogICAgZm9yICh2YXIgaT0wO2k8c2FtcGxlcy5sZW5ndGgtMTtpKyspIAogICAgICB7CiAgICAgICAgICBtYXggPSBzYW1wbGVzW2ldLlZWID4gbWF4ID8gc2FtcGxlc1tpXS5WVjptYXg7IC8vIENhbGN1bGF0aW5nIGFsbCB0aW1lIG1heGltdW0tLVdldCBpbmRleCAKICAgICAgICAgIG1pbiA9IHNhbXBsZXNbaV0uVlYgPCBtaW4gPyBzYW1wbGVzW2ldLlZWOm1pbjsgLy8gQ2FsY3VsYXRpbmcgYWxsIHRpbWUgbWluaW11bS0tRHJ5IGluZGV4IAogICAgICAgICAgc3VtX1ZWICs9IHNhbXBsZXNbaV0uVlY7IAogICAgICAgICAgY291bnQrKzsKICAgICAgfQogICAgLy8gT3ZlcmFsbCByYW5nZSBvZiBpbnRlbnNpdHkgdmFsdWVzIEFub2xvZ291cyB0byAwLTEwMCUgc29pbCBtb2lzdHVyZSAKICAgIHZhciBzZW5zaXRpdml0eSAgPSBtYXgtbWluOyAKICAgIC8vIElmIG92ZXJhbGwgYXZlcmdlIGlzIG1vcmUgdGhhbiA2ZEIgaS5lLiwgSGlnaCBpbnRlbnNpdHkgYWx3YXlzIHVzdWFsbHkgdXJiYW4gYXJlYXMuCiAgICAvLyBHZW5lcmF0aW5nIHVyYmFuIGFyZWEgbWFzayB1c2luZyAtNmRCIHRocmVzaG9sZAogICAgdXJiYW5fbWFzayA9IDEwKk1hdGgubG9nMTAoc3VtX1ZWL2NvdW50KSA%2BIC02ID8gIDAgOiAxOyAKICAgIC8vIElmIG92ZXJhbGwgYXZlcmdlIGlzIGxlc3MgdGhhbiAxN2RCIGkuZS4sIGxvdyBpbnRlbnNpdHkgYWx3YXlzIHVzdWFsbHkgd2F0ZXIgYm9kaWVzLgogICAgLy8gR2VuZXJhdGluZyBwZXJtYW5lbnQgd2F0ZXIgYm9keSBtYXNrIHVzaW5nIC0xN2RCIHRocmVzaG9sZAogICAgd2F0ZXJfbWFzayA9IDEwKk1hdGgubG9nMTAoc3VtX1ZWL2NvdW50KSA8IC0xNyA%2FICAwIDogMTsgCiAgICAvLyBBc3N1bWluZyBjaGFuZ2UgaW4gYmNrc2NhdHRlciBpbnRlbnNpdHkgb25seSBiZWNhdXNlIG9mIGNoYW5nZSBpbiBzb2lsIG1vaXN0dXJlLgogICAgTXYgPSAoKHNhbXBsZXNbMF0uVlYpIC0gbWluKS8oc2Vuc2l0aXZpdHkpOwogICAgTXYgPSBNdip3YXRlcl9tYXNrKnVyYmFuX21hc2s7Ly8gQXBwbHlpbmcgdXJiYW4gYW5kIHBlcm1hbmVudCB3YXRlciBib2R5IG1hc2sKCiAgICAvKgoKICAgIEFzc2lnbmluZyBjb2xvcm1hcCBmb3IgZW5oYW5jZWQgdmlzdWFsaXNhdGlvbgoKICAgICovCiAgICB2YXIgdiA9IE12OwogICAgdmFyIHZtaW4gPSAwOwogICAgdmFyIHZtYXggPSAwLjY7CiAgICB2YXIgZGlmZnYgPSB2bWF4IC0gdm1pbjsKICAgIAogICAgdmFyIHIgPSAwLjA7CiAgICB2YXIgZyA9IDAuMDsKICAgIHZhciBiID0gMC4wOwoKICAgIGlmICh2IDwgdm1pbil7CiAgICAgIHYgPSB2bWluOwogICAgfQogICAgaWYgKHYgPiB2bWF4KXsKICAgICAgdiA9IHZtYXg7CiAgICB9CiAgICAvL1RocmVzaG9sZCB2YWx1ZXMgZm9yIGNvbG9yTWFwCiAgICB2YXIgVDEgPSAwLjE7CiAgICB2YXIgVDIgPSAwLjM7CiAgICB2YXIgVDMgPSAwLjQ7CiAgICB2YXIgVDQgPSAwLjU7CiAgICAKICAgIHZhciBUaHJlc2hfMSA9ICh2bWluICsgVDEgKiBkaWZmdik7CiAgICB2YXIgVGhyZXNoXzIgPSAodm1pbiArIFQyICogZGlmZnYpOwogICAgdmFyIFRocmVzaF8zID0gKHZtaW4gKyBUMyAqIGRpZmZ2KTsKICAgIHZhciBUaHJlc2hfNCA9ICh2bWluICsgVDQgKiBkaWZmdik7CgogICAgaWYgKHYgPD0gMCkgCiAgICB7IAogICAgICByPTE7CiAgICAgIGc9MTsKICAgICAgYj0xOwogICAgfQogICAgZWxzZSBpZiAodiA8IFRocmVzaF8xKSAgIHsgIHIgPSAwLjUgKyAgKHYgLSB2bWluKSAvIChUaHJlc2hfMSAtIHZtaW4pIC8gMjsgfSAKICAgIGVsc2UgaWYgKHYgPCBUaHJlc2hfMikKICAgIHsKICAgICAgIHIgPSAxOwogICAgICAgZyA9ICh2IC0gVGhyZXNoXzEpIC8gKFRocmVzaF8yIC0gVGhyZXNoXzEpOwogICAgICAgYiA9IDA7CiAgICB9IAogICAgZWxzZSBpZiAodiA8IFRocmVzaF8zKSAKICAgIHsKICAgICAgIHIgPSAxICsgKFRocmVzaF8yIC0gdikgLyAoVGhyZXNoXzMgLSBUaHJlc2hfMik7CiAgICAgICBnID0gMTsKICAgICAgIGIgPSAodiAtIFRocmVzaF8yKSAvIChUaHJlc2hfMyAtIFRocmVzaF8yKTsKICAgIH0gCiAgICBlbHNlIGlmICh2IDwgVGhyZXNoXzQpCiAgICAgewogICAgICAgciA9IDA7CiAgICAgICBnID0gMSArIChUaHJlc2hfMyAtIHYpIC8gKFRocmVzaF80IC0gVGhyZXNoXzMpOwogICAgICAgYiA9IDE7CiAgICB9IAogICAgZWxzZSB7ICBiID0gMS4wICsgKFRocmVzaF80IC0gdikgLyAodm1heCAtIFRocmVzaF80KSAvIDI7ICB9CiAgICAgcmV0dXJuIFtyLCBnLCBiXTsKCiAgfQo%3D&temporal=true){:target="_blank"} 


## General description of the script

Script estimates surface soil moisture using change detection algorithm (TU Wien Change Detection model). The algorithm relates the change in backscatter intensity to the change in moisture. This relative change in soil moisture converted to absolute soil moisture by attributing the lowest and highest backscatter values to 0% and 100 % soil moisture respectively for a given pixel. To avoid the effect of outliers in caculating sensitivity of back scatter intensity (max-min), extreme 10% range on both sides was trimmed. This script produces soil moisture ranges from 0 to 60% with colour representation of red being 0 and blue as 60%. White colour represents the masked out area. Permanent water bodies and urban areas are masked out using backscatter intensity thresholds to minimise the number of false pixels. This masking approach is robust since it utilises long time series data.

## Details of the script

The script to estimate surface soil moisture using change detection approach can be applied globally. Since we are considering 3-year data in calculating the sensitivity of backscatter fluctuations,  it is resistant to seasonal fluctuations. It is capable of masking urban and permanent water bodies to reduce false results. The script can produce reasonably good results in flat and moderate slope terrains. But in high slope regions, the incidence angle effect on backscatter intensity affect the results. Rough water surfaces result in false results, e.g. oceans, but not always. Few developing urban areas may also produce false results.

For more details on the script see [supplementary material](supplementary_material.pdf).

## Author of the script

Narayana Rao Bhogapurapu

## Description of representative images

Resulted soil moisture is applied with jet color map for better interpretation. Red color represents low soil moisture (dry soil-0%) whereas blue represents high soil moisture (wet soil-60%). Permanent water bodies and built-up areas are masked out with white color.

Malinong, Australia
![The script example 1](fig/Malinong_Australia.jpg)

Manitoba, Canada
![The script example 2](fig/Manitoba_Canada.jpg)

Marrakech, Marocco
![The script example 3](fig/Marrakech_Morocco.jpg)

Sevilla, Spain
![The script example 3](fig/Sevilla_Spain.jpg)

Vijayawada, India
![The script example 3](fig/Vijayawada_India.jpg)

## References

[1] Wagner, W., Lemoine, G., Borgeaud, M. and Rott, H., 1999. A study of vegetation cover effects on ERS scatterometer data. IEEE Transactions on Geoscience and Remote Sensing, 37(2), pp.938-948.

[2] B. Bauer-Marschallinger et al.,  "Toward Global Soil Moisture Monitoring With Sentinel-1: Harnessing Assets and Overcoming Obstacles," in IEEE Transactions on Geoscience and Remote Sensing, vol. 57, no. 1, pp. 520-539, Jan. 2019.

## Credits

- Wagner, W., Lemoine, G., Borgeaud, M. and Rott, H., 1999. A study of vegetation cover effects on ERS scatterometer data. IEEE Transactions on Geoscience and Remote Sensing, 37(2), pp.938-948.

- B. Bauer-Marschallinger et al.,  "Toward Global Soil Moisture Monitoring With Sentinel-1: Harnessing Assets and Overcoming Obstacles," in IEEE Transactions on Geoscience and Remote Sensing, vol. 57, no. 1, pp. 520-539, Jan. 2019. 