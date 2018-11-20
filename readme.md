RHPAM HL7v2
=======================

A demo of RHPAM that takes in a message and allows a user to perform fixes. The updated message is sent to the specified callback URL.

## Required Group
The user task to update the message is assigned to the **hl7** group. Please make sure this group exists and your desired user is associated with that group.

## Example JSON to start the process
REST Endpoint: http://localhost:8080/kie-server/services/rest/server/containers/HL7v2_1.0.0/processes/HL7v2.FixMessage/instances
```
{
	"message": "MSH|^~\\&|MedOne|FACILITY A|CARECENTER^HL7NOTES|HFH|20060105180000| D61AFEF1-B10E-11D5-8666-0004ACD80749|MDM^T01|20060105180000999999|T|2.3\nEVN|T01|20060105180000\nPID|1||1112388^BS||ESPARZA^MARIA\nPV1|1|O|BS^15^15\nTXA|1|GENNOTES|TX|200601051800|50041^SMITH^CHRIS^M|200601051800|200601051800|200601051800|||\nSC^ROBINSON^JESSICA^A|1234567890||||FILE0001.TXT|PR",
	"callbackURL": "http://localhost:3030/callback"
}
```
