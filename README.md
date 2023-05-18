# Mod2 Week2 Assessment - Jeremy Kimball

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
Test Driven Development. It is the practice of writing the tests for code before actually writing any functioning code.
1. What are three benefits of using TDD?
Works almost like pseudocoding, allowing you to map the structure of the program you are creating.
When running into errors, the test suite gives better feedback than C# highlighting. (ie. telling you the exact values of certain variables)
You do not have to go back and write tests after the fact. Getting it out of the way in the beginning is nice as at the end you know your code is working properly and you dont need to write tests at the end (although you could think of more as you go)
1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
I use TDD to structure my code and lay out the expectations for how the program needs to properly function.
1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}

[Fact]
public void Dog_Constructor_InitializesDogObject()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
    Assert.Equal("Golden Retriever", dog.Breed);
    Assert.True(dog.IsHungry);
}

[Fact]
public void Dog_Eat_SetsIsHungryProperty()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat()
    Assert.False(dog.IsHungry);
}

[Fact]
public void Dog_Sleep_SetsIsHungryProperty()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Sleep()
    Assert.True(dog.IsHungry);
}

[Fact]
public void Dog_Speak_ReturnsString()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Bark Bark!", dog.Speak());
}
```

5. What is a merge conflict, and when might you encounter one?
A merge conflict is when two commits are editting the same line. You might encounter one when you are trying to merge a branch onto main that already has code where you have added some.
1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
On the main branch in github you (whether you are aa-branch or bb-branch) would submit a pull request, it would then be approved and merged. Afterwards, the other branch would also submit a pull request, if there were merge conflicts they would be resolved, approved, and then also merged to the main branch
1. Why is it good practice to have someone else approve and/or merge your PR?  
  Another set of eyes on your code is always a good idea, it allows for another fresh party to look over what you have written to make sure there would be no issues with merging the code into the main branch. 
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
