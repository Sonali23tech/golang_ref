
Go’s structs are typed collections of fields. They’re useful for grouping data together to form records.


Unlike maps , struct is value type
type Doctor struct {
    number int
    actorName string
    companions []string
}


func main(){
    aDoctor:= Doctor{
        number: 3 ,
        actorNmae : "Jon",
        companions : []string{
            "Sonali",
            "Sakshi",
            "Shekku",
        },

    }
    fmt.println(aDoctor)
}

Go doesn't support inheritance

Instead of inheritance go supports  Composition - Embedding

