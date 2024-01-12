# Erste-Schritte-MongoDB
### Datenbank erstellen oder auswählen
```use uni ```

### Collection erstellen und Universitäten hinzufügen
	 db.universities.insertMany([
	  { name: "Universität Zürich",city: "Zürich" },{ name: "ETH Zürich",city: "Zürich" },{ name: "Universität Genf", city: "Genf" },{ name: "EPFL Lausanne", city: "Lausanne" },{ name: "Universität Basel",city: "Basel" }
	])



### Alle Universitäten auflisten
``` db.universities.find()```

### Auf eine einzelne Uni per ID zugreifen 
```db.universities.findOne({ _id: ObjectId("65a12cdbf35e37ecefaaaf69!") })```

### Alle Universitäten einer bestimmten Stadt auflisten 
``` db.universities.find({ city: "Zürich" }) ```

### Universität nachträglich umbenennen 
```
db.universities.updateOne(
  { name: "Universität Zürich" },
  { $set: { name: "Neue Universität Zürich" } }
)
```
