# Data Models in Magic-UI

Magic-UI provides a flexible data model layer for working with local and remote structured data.  
Data models can be JSON- or CSV-based, automatically saved, and manipulated with built-in actions.

---

## 📂 Autosaving

- Data models are saved automatically in the **`Documents/SavedDataModels/`** folder.  
- Filename format: **`<name>_saved.json`** (where `name` is the data model key).  
- Saved models can be loaded **offline**.

---

## 📝 Supported Data Model Types

Each data model defines its own source (`DataModelSource` protocol). Currently supported types:

- `DataModelTypeJson`
- `DataModelTypeCsv`

### XML Declaration

If the `type` attribute is not provided, the default is **`json`**.

```xml
<datamodel key="countries" type="json" src="res:countries.json"/>
<datamodel key="excel" type="csv" src="url:https://magic-ui.com/Demo/DataModels/test.csv"/>

<!-- Create an empty model -->
<datamodel key="dmEmpty" type="json" src="new"/>
<datamodel key="dmEmpty" src="new"/>
