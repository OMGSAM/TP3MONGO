Récupérer tous les documents
 
db.collection.find().pretty()

Récupérer uniquement certains champs (par exemple nom et prenom) :
 
db.collection.find({}, { nom: 1, prenom: 1 })

Exclure un champ spécifique, par exemple age 

db.collection.find({}, { age: 0 })

Critère égalité (ex. : trouver tous les employés avec age = 30) :

db.collection.find({ age: 30 })

Critère supérieur ($gt) : Trouver les employés avec un sal > 2000 :

db.collection.find({ sal: { $gt: 2000 } })

Critère in : Rechercher des employés dans des villes spécifiques (ex. Casa ou Rabat) 

db.collection.find({ ville: { $in: ["Casa", "Rabat"] } })





 
// 1. Rechercher des noms commençant par "A"
db.collection.find({ nom: { $regex: "^A" } })

// 2. Rechercher des prénoms contenant "ah" (insensible à la casse)
db.collection.find({ prenom: { $regex: "ah", $options: "i" } })

// 3. Rechercher des prénoms terminant par "e"
db.collection.find({ prenom: { $regex: "e$" } })



  // Exercice 5 :  

// 1. Trier les employés par salaire (sal) en ordre décroissant
db.collection.find().sort({ sal: -1 })

// 2. Limiter les résultats aux 3 premiers
db.collection.find().sort({ sal: -1 }).limit(3)


// Exercice 6 :  

// 1. Nombre total de documents dans la collection
db.collection.countDocuments()

// 2. Salaire minimum et maximum
db.collection.aggregate([
  { $group: { _id: null, salaire_min: { $min: "$sal" }, salaire_max: { $max: "$sal" } } }
])

// 3. Salaire moyen
db.collection.aggregate([
  { $group: { _id: null, salaire_moyen: { $avg: "$sal" } } }
])


// Exercice 7 :  

// 1. Trouver les employés dont l'âge est supérieur à 25 et qui habitent à Casablanca
db.collection.find({ $and: [{ age: { $gt: 25 } }, { ville: "Casa" }] })

// 2. Trouver les employés dont le prénom commence par "M" ou qui gagnent plus de 3000
db.collection.find({
  $or: [{ prenom: { $regex: "^M" } }, { sal: { $gt: 3000 } }]
})


// Exercice 8 : Suppression et mise à jour

// 1. Supprimer un document avec un critère (par exemple, code = 5)
db.collection.deleteOne({ code: 5 })

// 2. Mettre à jour un document (augmenter le salaire de 500 pour code = 2)
db.collection.updateOne(
  { code: 2 },
  { $inc: { sal: 500 } }
)





