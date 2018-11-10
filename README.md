# CSharpSnippets
Useful Snippets for Visual Studio - C# 

## MVVM Pattern Snippets
### OpenMVVM
#### mprop snippet
Creates prop with backing field, also rising property changed event.
Example:
```csharp
private string customerFirstName;

public string CustomerFirstName
{
    get => this.customerFirstName;
    set => this.Set(ref this.customerFirstName, value);
}
```
#### mcomm snippet
Creates ICommand prop with backing field.
Example:
```csharp
private IMvvmCommand nextPageCommand;

public IMvvmCommand NextPageCommand => this.nextPageCommand ?? (this.nextPageCommand = new ActionCommand(() => { }));
```
### Prism
#### pprop snippet
Creates prop with backing field, also rising property changed event.
Example:
```csharp
private string customerFirstName;

public string CustomerFirstName
{
    get => this.customerFirstName;
    set => this.SetProperty(ref this.customerFirstName, value);
}
```
#### pcomm snippet
Creates ICommand prop with backing field.
Example:
```csharp
private ICommand nextPageCommand;

public ICommand NextPageCommand => this.nextPageCommand ?? (this.nextPageCommand = new DelegateCommand(() => { }));
```
