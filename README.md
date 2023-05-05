Original C#:

public class Dog
{
	public string Name { get; set; }
	public string Breed { get; set; }

	public Dog(string name, string breed)
	{
    	Name = name;
    	Breed = breed;
	}

	public string Bark()
	{
    	return "Woof!";
	}
}

string[] dogBreeds = new string[] { "Labrador", "Golden Retriever", "Bulldog" };

public string GetRandomBreed(string[] breeds)
{
	Random random = new Random();
	int index = random.Next(breeds.Length);
	return breeds[index];
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Version:

class Dog {
  constructor(name, breed) {
    this.name = name;
    this.breed = breed;
  }

  bark() {
    return "Woof!";
  }
}

const dogBreeds = ["Labrador", "Golden Retriever", "Bulldog"];

function getRandomBreed(breeds) {
  const random = Math.floor(Math.random() * breeds.length);
  return breeds[random];
}

// Test the code
const randomBreed = getRandomBreed(dogBreeds);
console.log("Random breed:", randomBreed);

const dog = new Dog("Buddy", randomBreed);
console.log("Dog's name:", dog.name);
console.log("Dog's breed:", dog.breed);
console.log("Dog barks:", dog.bark());




---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
TypeScript Version:

class Dog {
  name: string;
  breed: string;

  constructor(name: string, breed: string) {
    this.name = name;
    this.breed = breed;
  }

  bark(): string {
    return "Woof!";
  }
}

const dogBreeds: string[] = ["Labrador", "Golden Retriever", "Bulldog"];

function getRandomBreed(breeds: string[]): string {
  const index: number = Math.floor(Math.random() * breeds.length);
  return breeds[index];
}

// Test the Dog class and getRandomBreed function
const randomBreed = getRandomBreed(dogBreeds);
const myDog = new Dog("Buddy", randomBreed);

console.log(`Dog name: ${myDog.name}`);
console.log(`Dog breed: ${myDog.breed}`);
console.log(`Dog bark: ${myDog.bark()}`);
