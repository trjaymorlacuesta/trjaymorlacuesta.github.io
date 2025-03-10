---
category: Web Service Calls
path: '/msg/getSettlementDateSoldBy'
title: 'getSettlementDateSoldBy'
type: 'POST'

layout: nil
---

# getSettlementDateSoldBy

##Overview
This call is used to fetch the settlement date and sold by fields coming from property service of BSGv3 that aren't available on BSGv2.

<table>
	<tbody>
	<tr>
		<th>BSGv3</th>
		<th>BSGv2</th>
		<th>Show Additional Data Elements</th>
	</tr>
	<tr>
		<td>Yes</td>
		<td>No</td>
		<td></td>
	</tr>

</tbody>
</table>

### Additional Information

For further reading regarding BSG Elements: 

* [Property Detail Service](http://confluence.rpdata.local/display/BA/Property+Detail+Service)

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
		<td>propertyId</td>
		<td>Property Id</td>
		<td>Yes</td>
		
	</tr>
</tbody>
</table>

***Sample Request***
```{
    "op": "getSettlementDateSoldBy",
    "uid": "TWISTUSER001",
    "sid": "2-4eed242594fc464787b8054ddc77de11",
    "propertyId": "3604024"
}```

### Response

Success:
```{
  "response": {
    "status": "success",
    "result": {
      "settlementDate": "27/04/2010",
      "soldBy": "Hamilton & Co Lane Cove"
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