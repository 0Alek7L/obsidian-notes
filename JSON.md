#EntityFramework 

==JSON==
--
using **System.Text.Json**
using **System.Text.Json.Serialization**

string result = JsonSerializer.Serialize(//object//, );
File.WriteAllText("object.json", result);

string json = File.ReadAllText("object.json");
var newObject = JsonSerializer.Deserialize<\Person>(json);

==JSON.NET==
--

**SERIALIZATION OPTIONS ->** https://prnt.sc/hqJ9OFU8qOrb
