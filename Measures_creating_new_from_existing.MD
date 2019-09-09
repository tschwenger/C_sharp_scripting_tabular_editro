# This File contains script snippets to create new measures in the Tabular Editor


## Create new measures from selected measures


        foreach(var m in Selected.Measures)
        {
                m.Table.AddMeasure(
                    m.Name + "ABC",
                    "Calculate(" + m.DaxObjectName + ", DimBusinessUnit[Channel]=" + "ABC" +")",
                    m.DisplayFolder
                );
                m.IsHidden=false;
            }
            
            
This script will loop over all the measures selected in the tabular editor and create a new measure based on the old measure's name (adding "ABC"),
then creates the dax script applying calculated, and filtering the table to that specific dimension attribute. The script then places the 
new measure in the same display folder and keeps the measure visible. 
