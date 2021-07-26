# Xamarin.Forms.Helpers
### Converters
**1.IsNegatedValueConverter**
> Returns true if value of referenced binding property is false and vice-versa. 

Used in scenarios such as   
1. If you have to show some content while a property is set to true and show another view while same property is false. In such scenario, instead of creating two different bindable properties, create a single bindable property and use this converter


**2.IsValueMatchedConverter**
> Returns true if a string value matches with another comparable value

Used in scenarios such as
1. Show a bindable object if value of a binding property/static field matches with another binding property/static field value. 

**3.IsValueNotMatchedConverter**
> Returns true if a string value doesnot doesnot match with another comparable value

Used in scenario such as
1. Show a bindable object if value of a binding property/static field doesnot match another binding property/static field value.
