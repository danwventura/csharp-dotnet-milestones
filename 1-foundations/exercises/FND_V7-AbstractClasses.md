# Zoolandia - Abstract Classes

## Setup

```bash
cd ~/workspace/zoolandia
git checkout -b version-7
```

## Instructions

Your job is to use abstract classes to create a class that is to hold properties and methods that an sub class will inherit. Some properties and methods will
be used as written in the abstract class other propeties and methods will be overridden. Abstract classes cannot be instanciated, only inherited from
classes can implement only one abstract class but can also inherit from more than one interface

* An abstract class of FishType can be implemented by one the class called Agnatha. There are three main fish types so Agnatha, Chrondrichthyes,
and Osteichthyes all inherit from FishType.
```

    class Agnatha : FishType, IFishSpecies, IHabitat
    {
        public int AverageLifeSpan { get; set; }
        public override string CommonName { get; set; }
        public override string ScientificName { get; set; }
        ...
        
         class Hagfish: Agnatha
    {
```Create a new Hagfish Object
```
         Agnatha hagFish = new Agnatha
            {
                CommonName = "Hagfish",
                ScientificName = "Eptatretus stoutii",
                DepthLevel = "Deep Oceans",
                WaterType="Salt Water though some part of lifecycle spent fresh water.",
                FinDescription = new FinDetails
                {
                    CaudalKeelDescription= "absent",
                    PectorialFinDescription="absent",
                    DorsalFinDescription="absent",
                    AnalFinDescription="absent",
                    AdiposeFinDescription="absent in most",
                    FinletsDescription="absent"
                },
               FishTypeCommonName=fishtypes.Agnathan.ToString(),
            };
```
Output the set properties

```
 hagfish.LongDescription = hagfish.GetLongDescription();
 Console.Write("Common Name is " + hagfish.CommonName);
```
