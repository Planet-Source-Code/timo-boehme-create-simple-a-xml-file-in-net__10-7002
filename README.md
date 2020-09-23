<div align="center">

## Create simple a Xml file in \.Net


</div>

### Description

Create your XML file by using the included XML classes in Visual Studio.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Timo Boehme](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/timo-boehme.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |C\#, VB\.NET, ASP\.NET
**Category**       |[Databases](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/databases__10-5.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/timo-boehme-create-simple-a-xml-file-in-net__10-7002/archive/master.zip)





### Source Code

```
Dim XmlDoc As New XmlDocument
    'Write down the XML declaration
    Dim XmlDeclaration As XmlDeclaration = XmlDoc.CreateXmlDeclaration("1.0", "UTF-8", Nothing)
    'Create the root element
    Dim RootNode As XmlElement = XmlDoc.CreateElement("RootNode")
    XmlDoc.InsertBefore(XmlDeclaration, XmlDoc.DocumentElement)
    XmlDoc.AppendChild(RootNode)
    'Create a new <Category> element and add it to the root node
    Dim ParentNode As XmlElement = XmlDoc.CreateElement("Parent")
    'Set attribute name and value!
    ParentNode.SetAttribute("AttributName", "AttributWert")
    XmlDoc.DocumentElement.PrependChild(ParentNode)
    'Create the required nodes
    Dim FirstElement As XmlElement = XmlDoc.CreateElement("FirstElement")
    Dim SecondElement As XmlElement = XmlDoc.CreateElement("SecondElement")
    Dim ThirdElement As XmlElement = XmlDoc.CreateElement("ThirdElement")
    'retrieve the text
    Dim FirstTextElement As XmlText = XmlDoc.CreateTextNode("This is the text from the first element")
    Dim SecondTextElement As XmlText = XmlDoc.CreateTextNode("This is the text from the second element")
    Dim ThirdTextElement As XmlText = XmlDoc.CreateTextNode("This is the text from the third element")
    'append the nodes to the parentNode without the value
    ParentNode.AppendChild(FirstElement)
    ParentNode.AppendChild(SecondElement)
    ParentNode.AppendChild(ThirdElement)
    'save the value of the fields into the nodes
    FirstElement.AppendChild(FirstTextElement)
    SecondElement.AppendChild(SecondTextElement)
    ThirdElement.AppendChild(ThirdTextElement)
    'Save to the XML file
    XmlDoc.Save("demo.xml")
```

