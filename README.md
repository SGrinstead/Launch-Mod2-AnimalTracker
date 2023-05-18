# Mod2 Week2 Assessment - Seth Grinstead

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
    TDD stands for Test Driven Development. It is the practice of writing the tests for your code first, then writing the code to make those tests pass.

1. What are three benefits of using TDD?
    1. When you write the tests first, it doesn't feel like a chore you have to do later
    2. It makes you think ahead of time about what you need to write and make descisions early
    3. You only end up making the code you need. Because you outline it with tests, you know when you don't need to add anything more

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
    I use TDD to plan out my code ahead of time. By writing the tests, I get a strong idea about what I want the code to look like and when it will be finished.

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
[Fact]
public void Dog_Eat_SetsIsHungryToFalse()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    dog.Eat();

    Assert.False(dog.IsHungry);
}

[Fact]
public void Dog_Sleep_SetsIsHungryToTrue()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    dog.Eat();
    dog.Sleep();

    Assert.True(dog.IsHungry);
}

[Fact]
public void Dog_Speak_ReturnsString()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Bark Bark!", dog.Speak());
}

[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}
```

5. What is a merge conflict, and when might you encounter one?
    A merge conflict happens when you try to merge branches with changes on the same line. This could happen when two people are working on branches that both make changes in one file and they try to merge both.

1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
    We would each commit and push the branch, then each submit a pull request to merge the branch back into the main branch. We would review eachothers pull requests and approve any changes, then 
    merge the branches into main, resolving any merge cconflicts along the way.

1. Why is it good practice to have someone else approve and/or merge your PR?
    You want to let other people review your changes so everyone can be on the same page about any changes that you have made. They can also suggest changes to make before you merge.
  
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
