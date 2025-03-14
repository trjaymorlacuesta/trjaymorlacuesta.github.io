---
category: Web Service Calls
path: '/msg/getPhotoGallery'
title: 'getPhotoGallery'
type: 'POST'

layout: nil
---

# getPhotoGallery

##Overview
This call is used to fetch the photos, aerial map, area map and topo map of the given property; it uses the BSGv2's getPhotos, getAerialMap, getAreaMap and getTopoMap under Property Imagery Service.

<table>
	<tbody>
	<tr>
		<th>BSGv3</th>
		<th>BSGv2</th>
		<th>Show Additional Data Elements</th>
	</tr>
	<tr>
		<td>No</td>
		<td>Yes</td>
		<td></td>
	</tr>

</tbody>
</table>

### Additional Information

For further reading regarding BSG Elements: 

* [Method_getPhotos](http://confluence.rpdata.local/display/BA/Method_getPhotos)

### Request

***Parameters***

<table>
	<tbody>
	<tr>
		<th>Parameter</th>
		<th>Description</th>
		<th>Required</th>
		
	</tr>
	<tr>
		<td>op</td>
		<td>Operation</td>
		<td>Yes</td>
		
	</tr>
	<tr>
		<td>uid</td>
		<td>User ID</td>
		<td>Yes</td>
		
	</tr>
	<tr>
		<td>sid</td>
		<td>Session ID</td>
		<td>Yes</td>
		
	</tr>
	<tr>
		<td>id</td>
		<td>Property ID</td>
		<td>Yes</td>
		
	</tr>
	<tr>
		<td>displayMapUrl</td>
		<td>Display Map Url</td>
		<td>No</td>
		
	</tr>
</tbody>
</table>

***Sample Request***
```{
    "op": "getphotogallery",
    "uid": "TWISTUSER001",
    "sid": "2-4eed242594fc464787b8054ddc77de11",
    "id": "7007180"
}```

### Response

Success:
```{
  "response": {
    "status": "success",
    "result": {
      "photos": [
        {
          "smallImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/320x215/09/11/06/16554835/16554835_1.JPG",
          "mediumImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/470x313/09/11/06/16554835/16554835_1.JPG",
          "largeImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/768x512/09/11/06/16554835/16554835_1.JPG"
        },
        {
          "smallImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/320x215/09/11/06/16554835/16554835_2.JPG",
          "mediumImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/470x313/09/11/06/16554835/16554835_2.JPG",
          "largeImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/768x512/09/11/06/16554835/16554835_2.JPG"
        },
        {
          "smallImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/320x215/09/11/06/16554835/16554835_3.JPG",
          "mediumImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/470x313/09/11/06/16554835/16554835_3.JPG",
          "largeImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/768x512/09/11/06/16554835/16554835_3.JPG"
        },
        {
          "smallImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/320x215/09/11/06/16554835/16554835_4.JPG",
          "mediumImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/470x313/09/11/06/16554835/16554835_4.JPG",
          "largeImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/768x512/09/11/06/16554835/16554835_4.JPG"
        },
        {
          "smallImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/320x215/04/07/19/NSW00925A/473.JPG",
          "mediumImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/470x313/04/07/19/NSW00925A/473.JPG",
          "largeImageDisplayURL": "https://static.rpdata.com/rpdaAU/photo/listsale/768x512/04/07/19/NSW00925A/473.JPG"
        }
      ],
      "aerialMap": "https://rpp.rpdata.com/rpmapAU/servlet/GenMap?mapView=AERIAL&mapSource=NSW&propertyId=47287106&user=rpdata&propertyPerimeter=true&mapSize=560x420&roads=true&roadNames=true&propertyNumbers=true&lots=true&propertyMeasurements=true&water=true&parks=true&rails=true&lotAreas=false",
      "areaMap": "https://static.rpdata.com/rpdaAU/areamap/nsw/2074/turramurra.gif",
      "topoMap": "https://rpp.rpdata.com/rpmapAU/servlet/GenMap?mapView=CADASTRE&mapSource=NSW&propertyId=47287106&user=rpdata&propertyPerimeter=true&mapSize=560x420&roads=true&roadNames=true&propertyNumbers=true&lots=true&propertyMeasurements=true&water=true&parks=true&rails=true&lotAreas=false&lotPlan=false&easements=false"
    }
  }
}```

Error:
```{
    "response": {
        "status": "error",
        "description": "error description"
    }
}```