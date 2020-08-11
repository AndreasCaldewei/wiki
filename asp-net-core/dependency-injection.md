### Dependency Injection
#### Basic
First of all create an interface which describes the shape of our dependency.
```csharp
public interface IEmployeRepository
{
    Employee GetEmployee(int Id)
}
```
After that create an implementation of the interface.
```csharp
   public class EmployeMockRepository : IEmployeRepository
    {
        public Employee GetEmployee(int Id)
        {
            return new Employee();
        }
    }
```
And register your dependency in the app Startup.
```csharp
... 
public void ConfigureServices(IServiceCollection services)
    {
        ...
        services.AddSingleton<IEmployeRepository, EmployeMockRepository>();
    }
...
```



