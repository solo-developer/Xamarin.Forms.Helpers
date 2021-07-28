# Xamarin.Forms.Helpers
### Converters

#### First Step

a. Import namespace in Xaml 
``` xmlns:converters="clr-namespace:XmartCreditMobileApp.Converters" ```
   
b. Add a key in ContentPage Resources

```<ContentPage.Resources>  
      <ResourceDictionary>  
        <converters:IsNegatedValueConverter x:Key="NegateBool" />    
        <converters:IsValueNotMatchedConverter x:Key="IsValueNotMatchedConverter" />
      </ResourceDictionary>  
   </ContentPage.Resources>
```
   
**1.IsNegatedValueConverter**
> Returns true if value of referenced binding property is false and vice-versa. 

Used in scenarios such as   
1. If you have to show some content while a property is set to true and show another view while same property is false. In such scenario, instead of creating two different bindable properties, create a single bindable property and use this converter

**Usage**  
```<ImageButton IsEnabled="{Binding IsBusy,Converter={StaticResource NegateBool},ConverterParameter={Binding IsBusy}}"/>  ```
    
**2.IsValueMatchedConverter**
> Returns true if a string value matches with another comparable value

Used in scenarios such as
1. Show a bindable object if value of a binding property/static field matches with another binding property/static field value. 
 

**3.IsValueNotMatchedConverter**
> Returns true if a string value doesnot doesnot match with another comparable value

Used in scenario such as
1. Show a bindable object if value of a binding property/static field doesnot match another binding property/static field value.

**Usage**
 ```<Image.IsVisible>
      <MultiBinding Converter="{StaticResource IsValueNotMatchedConverter}">
         <Binding Path="string_binding_field_1" />
         <Binding Path="string_binding_field_2" />
      </MultiBinding>
     </Image.IsVisible> 
    
