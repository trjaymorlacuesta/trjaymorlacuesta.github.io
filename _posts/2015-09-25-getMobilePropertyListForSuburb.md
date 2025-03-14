---
category: Web Service Calls
path: '/msg/getMobilePropertyListForSuburb'
title: 'getMobilePropertyListForSuburb'
type: 'POST'

layout: nil
---

# getMobilePropertyListForSuburb

##Overview
This call is used to fetch all property details from the given suburb, it uses BSGv2's Search method. Results can be filtered by the status of the property such as for sale, for rent or sales. 

When the showAdditionalDataElements is true, it will use the BSGv3's property service to show the additional fields that aren't available on BSGv2.

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
		<td>Yes</td>
	</tr>

</tbody>
</table>

### Additional Information

For further reading regarding BSG Elements: 

* [Method_getPropertyIdListFromSuggestion](http://confluence.rpdata.local/display/BA/Method_getPropertyIdListFromSuggestion)
* [Method_search](http://confluence.rpdata.local/display/BA/Method_search)

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
		<td>postcode</td>
		<td>Postcode</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>suburb</td>
		<td>Suburb</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>state</td>
		<td>State</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>maxResult</td>
		<td>Maximum Result</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>priceMin</td>
		<td>Price Minimum</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>priceMax</td>
		<td>Price Maximum</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>bedrooms</td>
		<td>Number of Bedrooms</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>bathrooms</td>
		<td>Number of Bathrooms</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>parking</td>
		<td>Parking</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>landSize</td>
		<td>Land Size</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>floorSize</td>
		<td>Floor Size</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>capitalValueMin</td>
		<td>Capital Value Minimum</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>capitalValueMax</td>
		<td>Capital Value Maximum</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>start</td>
		<td>Start</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>house</td>
		<td>Having House Property Type</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>unit</td>
        <td>Having Unit Property Type</td>
        <td>Yes</td>
		
	</tr>
	<tr>
		<td>land</td>
		<td>Land</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>commercial</td>
		<td>Commercial</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>others</td>
		<td>Others</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>recentlySold</td>
		<td>Recently Sold</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>forSale</td>
		<td>For Sale</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>other</td>
		<td>Other</td>
        <td>Yes</td>
        
	</tr>
	<tr>
		<td>forRentOnly</td>
		<td>For Rent Only</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>listedDays</td>
		<td>Listed Days</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>soldDays</td>
		<td>Sold Days</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>pageNumber</td>
		<td>Page Number</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>pageSize</td>
		<td>Page Size</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>isSortedByAddress</td>
		<td>Is Sorted By Address</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>showAdditionalDataElements</td>
		<td>Show Additional Data Elements</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>sortBy</td>
		<td>Sort By</td>
        <td>No</td>
        
	</tr>
	<tr>
		<td>sortOrder</td>
		<td>Sort Order</td>
        <td>No</td>
        
	</tr>
</tbody>
</table>

***Sample Request***
```{
    "op": "getMobilePropertyListForSuburb", 
    "uid": "TWISTUSER001",
    "sid": "2-4eed242594fc464787b8054ddc77de11",
    "state": "NSW", 
    "suburb": "NEWTOWN", 
    "postcode": "2042", 
    "maxResult": "5", 
    "start": "1", 
    "house": "true", 
    "unit": "true", 
    "recentlySold": "true", 
    "forSale": "true", 
    "other": "true", 
    "landSize": "0", 
    "bedrooms": "0", 
    "bathrooms": "0"
}```

### Response

Success:
```{
  "response": {
    "status": "success",
    "result": {
      "summary": {
        "total": 7665,
        "onTheMarket": 35,
        "recentlySold": 156,
        "other": 7311,
        "isLastPage": false,
        "forRent": 163
      },
      "pages": {
        "totalPages": 1533,
        "currentPage": 1
      },
      "buildings": [],
      "properties": [
        {
          "type": "House",
          "id": 4879567,
          "lat": -33.8960781,
          "lon": 151.17397436,
          "unitNumber": "",
          "streetNumber": "101",
          "streetName": "Albermarle",
          "streetType": "Street",
          "streetDirection": "",
          "address": "101 Albermarle Street",
          "suburb": "Newtown",
          "postcode": "2042",
          "state": "NSW",
          "bathrooms": 1,
          "bedrooms": 3,
          "parking": 1,
          "landSize": 108,
          "salePrice": "800000",
          "saleDate": "20/10/2009",
          "onTheMarket": true,
          "listingDate": "08/11/2015",
          "listingPrice": "1365000",
          "listingDescription": "for sale - $1,365,000",
          "REAId": "120922385",
          "agentName": "-",
          "recentSales": false,
          "photo": "https://static.rpdata.com/rpdaAU/photo/listsale/120x80/15/10/07/26128001/26128001_1.JPG",
          "ucv": 79700,
          "ucvDate": "01/07/1997",
          "realPropertyDescriptor": "LOT 6 DP108105",
          "lgaName": "Marrickville",
          "lastSaleType": "Unknown",
          "lotPlan": "6/DP108105 NEWTOWN NSW",
          "zoning": "Residential",
          "isAgentAdvised": false,
          "landUsePrimary": "Single Res Dwelling",
          "currentRentalPrice": "",
          "forRent": false,
          "forRentDaysOnMarket": 0,
          "forRentAgencyName": "",
          "occupancyType": "",
          "volume": "",
          "folio": "",
          "mapReference": "",
          "block": "",
          "section": ""
        },
        {
          "type": "House",
          "id": 4880325,
          "lat": -33.90459885,
          "lon": 151.17384184,
          "unitNumber": "",
          "streetNumber": "181",
          "streetName": "Alice",
          "streetType": "Street",
          "streetDirection": "",
          "address": "181 Alice Street",
          "suburb": "Newtown",
          "postcode": "2042",
          "state": "NSW",
          "bathrooms": 2,
          "bedrooms": 4,
          "parking": 2,
          "landSize": 143,
          "salePrice": "453000",
          "saleDate": "16/08/2000",
          "onTheMarket": true,
          "listingDate": "30/10/2015",
          "listingPrice": "0",
          "listingDescription": "Expressions Of Interest",
          "REAId": "",
          "agentName": "-",
          "recentSales": false,
          "photo": "https://static.rpdata.com/rpdaAU/photo/listsale/120x80/15/10/04/26116905/26116905_1.JPG",
          "ucv": 79700,
          "ucvDate": "01/07/1997",
          "realPropertyDescriptor": "LOT B DP 107528",
          "lgaName": "Marrickville",
          "lastSaleType": "Unknown",
          "lotPlan": "B/DP107528 NEWTOWN NSW",
          "zoning": "Residential",
          "isAgentAdvised": false,
          "landUsePrimary": "Single Res Dwelling",
          "currentRentalPrice": "",
          "forRent": false,
          "forRentDaysOnMarket": 0,
          "forRentAgencyName": "",
          "occupancyType": "",
          "volume": "",
          "folio": "",
          "mapReference": "",
          "block": "",
          "section": ""
        },
        {
          "type": "House",
          "id": 4880475,
          "lat": -33.90170103,
          "lon": 151.18013781,
          "unitNumber": "",
          "streetNumber": "88",
          "streetName": "Angel",
          "streetType": "Street",
          "streetDirection": "",
          "address": "88 Angel Street",
          "suburb": "Newtown",
          "postcode": "2042",
          "state": "NSW",
          "bathrooms": 2,
          "bedrooms": 3,
          "parking": 1,
          "landSize": 500,
          "salePrice": "1025000",
          "saleDate": "09/02/2005",
          "onTheMarket": true,
          "listingDate": "06/11/2015",
          "listingPrice": "0",
          "listingDescription": "POA",
          "REAId": "118534859",
          "agentName": "-",
          "recentSales": false,
          "photo": "https://static.rpdata.com/rpdaAU/photo/listsale/120x80/14/11/20/24848096/24848096_1.JPG",
          "ucv": 195000,
          "ucvDate": "01/01/1930",
          "realPropertyDescriptor": "LOT 1 DP1147071",
          "lgaName": "Sydney",
          "lastSaleType": "Unknown",
          "lotPlan": "2/DP456893 NEWTOWN NSW",
          "zoning": "Residential",
          "isAgentAdvised": false,
          "landUsePrimary": "Single Res Dwelling",
          "currentRentalPrice": "",
          "forRent": false,
          "forRentDaysOnMarket": 0,
          "forRentAgencyName": "",
          "occupancyType": "",
          "volume": "",
          "folio": "",
          "mapReference": "",
          "block": "",
          "section": ""
        },
        {
          "type": "House",
          "id": 4880927,
          "lat": -33.89538037,
          "lon": 151.17421721,
          "unitNumber": "",
          "streetNumber": "41",
          "streetName": "Baltic",
          "streetType": "Street",
          "streetDirection": "",
          "address": "41 Baltic Street",
          "suburb": "Newtown",
          "postcode": "2042",
          "state": "NSW",
          "bathrooms": 1,
          "bedrooms": 2,
          "parking": 0,
          "landSize": 121,
          "salePrice": "320000",
          "saleDate": "27/05/1999",
          "onTheMarket": true,
          "listingDate": "08/11/2015",
          "listingPrice": "0",
          "listingDescription": "Auction",
          "REAId": "121113930",
          "agentName": "-",
          "recentSales": false,
          "photo": "https://static.rpdata.com/rpdaAU/photo/listsale/120x80/15/10/27/26223392/26223392_1.JPG",
          "ucv": 82500,
          "ucvDate": "01/07/1997",
          "realPropertyDescriptor": "LOT 2 DP 110260",
          "lgaName": "Marrickville",
          "lastSaleType": "Unknown",
          "lotPlan": "2/DP110260 NEWTOWN NSW",
          "zoning": "Residential",
          "isAgentAdvised": false,
          "landUsePrimary": "Single Res Dwelling",
          "currentRentalPrice": "",
          "forRent": false,
          "forRentDaysOnMarket": 0,
          "forRentAgencyName": "",
          "occupancyType": "",
          "volume": "",
          "folio": "",
          "mapReference": "",
          "block": "",
          "section": ""
        },
        {
          "type": "House",
          "id": 4881008,
          "lat": -33.89686264,
          "lon": 151.17512012,
          "unitNumber": "",
          "streetNumber": "67",
          "streetName": "Bedford",
          "streetType": "Street",
          "streetDirection": "",
          "address": "67 Bedford Street",
          "suburb": "Newtown",
          "postcode": "2042",
          "state": "NSW",
          "bathrooms": 1,
          "bedrooms": 1,
          "parking": 0,
          "landSize": 70,
          "salePrice": "527000",
          "saleDate": "22/07/2011",
          "onTheMarket": true,
          "listingDate": "10/11/2015",
          "listingPrice": "0",
          "listingDescription": "auction",
          "REAId": "121071226",
          "agentName": "-",
          "recentSales": false,
          "photo": "https://static.rpdata.com/rpdaAU/photo/listsale/120x80/15/10/22/26203025/26203025_1.JPG",
          "ucv": 66000,
          "ucvDate": "01/07/1997",
          "realPropertyDescriptor": "LOT 5 DP219642",
          "lgaName": "Marrickville",
          "lastSaleType": "Unknown",
          "lotPlan": "5/DP219642 NEWTOWN NSW",
          "zoning": "Residential",
          "isAgentAdvised": false,
          "landUsePrimary": "Single Res Dwelling",
          "currentRentalPrice": "",
          "forRent": false,
          "forRentDaysOnMarket": 0,
          "forRentAgencyName": "",
          "occupancyType": "",
          "volume": "",
          "folio": "",
          "mapReference": "",
          "block": "",
          "section": ""
        }
      ]
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