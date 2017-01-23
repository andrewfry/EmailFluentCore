# EmailFluentCore  
Migrated EmailFluent to dot net core. The original page: https://github.com/lukencode/FluentEmail


Example usage from:
```
var email = Email
        .From("john@email.com")
        .To("bob@email.com", "bob")
        .Subject("hows it going bob")
        .TextBody("yo dawg, sup?");
```
        
Templates usage:
```
var template = "Dear @Model.Name, You are totally @Model.Compliment.";

var email = Email
    .From("bob@hotmail.com")
    .To("somedude@gmail.com")
    .Subject("woo nuget")
    .UsingTemplate(template, new { Name = "Luke", Compliment = "Awesome" });
```

Sending:
```
//send normally
email.Send();

//send asynchronously
email.SendAsync();
```
