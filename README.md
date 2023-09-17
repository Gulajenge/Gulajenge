- 👋 Hi, I’m @Gulajenge
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Gulajenge/Gulajenge is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---> section HelloWorld;
 
[DataSource.Kind="HelloWorld", Publish="HelloWorld.Publish"]
shared HelloWorld.Contents = (optional message as text) =>
    let
        message = if (message <> null) then message else "Hello world"
    in
        message;
 
HelloWorld = [
    Authentication = [
        Implicit = []
    ],
    Label = Extension.LoadString("DataSourceLabel")
];
 
HelloWorld.Publish = [
    Beta = true,
    ButtonText = { Extension.LoadString("FormulaTitle"), Extension.LoadString("FormulaHelp") },
    SourceImage = HelloWorld.Icons,
    SourceTypeImage = HelloWorld.Icons
];
 
HelloWorld.Icons = [
    Icon16 = { Extension.Contents("HelloWorld16.png"), Extension.Contents("HelloWorld20.png"), Extension.Contents("HelloWorld24.png"), Extension.Contents("HelloWorld32.png") },
    Icon32 = { Extension.Contents("HelloWorld32.png"), Extension.Contents("HelloWorld40.png"), Extension.Contents("HelloWorld48.png"), Extension.Contents("HelloWorld64.png") }
];
