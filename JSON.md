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

changing the properties' names for the serialization -> https://prnt.sc/DF_B_VULDx-9 