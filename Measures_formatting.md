# Formatting Measures

This is meant to be a quick reference for creating script snippet for advanced scripting in the tabular editor

### US currency

            Selected.Measures.ForEach(m=>m.FormatString="$ #,##0.0");

The above code changes all selected measures to US currency with one decimal and a thousands separator

### Euro Currency

            Selected.Measures.ForEach(m=>m.FormatString="€ #,##0.00");
      
this above code will change all selected measures to euro currency with a thousands separator and two decimals
