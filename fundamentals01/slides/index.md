- title : Dependencies
- description : Introduction to modern dotNET application development
- author : Martin Schinz
- theme : league
- transition : default

***

### Properties of maintainable software solutions

![cat in heaven](images/cat_in_heaven.gif)

- Easy to change
- Easy to evolve / extend
- Easy to test

How do we get there?

***

- Modularity
- Design for Replaceability
- Depend on Interfaces instead of Implementations

***

### The problem

#### You might have done this:

    [lang=cs]
    public class CatLoader {
        public Cat[] Load() {
            var dbContext = new DbContext();
            var cats = dbContext.Query<Cat[]>().All();
            return cats;
        }
    }

What could be wrong with that?

***
### Problems with inline dependencies

- Testing
- Dependency configuration
- Dependency lifetime

***

### Testing

- Create a database
- Seed it with all the data</li>
- Create testing credentials
- Assert on loaded cats

---

##### Configure the Context differently

- Will need to change at all call sites
- Process to ensure everyone follows convention

---

##### Pool the resources for the Context

- Change DbContext implementation


---

![Glued](./images/glued_together.gif)

### Can we do better?


***

### Make dependencies explicit and external

Benefits

- Test against any result we want
- Configure the dependency globally
- Decide on the lifetime of the dependency

***

### Examples

- Method parameterization
- Constructor parameterization

---

#### Method parameterization

    [lang=cs]
    public class CatLoader {
        public Cat[] Load(DbContext dbContext) {
            var cats = dbContext.Query<Cat[]>().All();
            return cats;
        }
    }

#### Constructor parameterization

    [lang=cs]

    public class CatLoader {
        private DbContext dbContext = null;
        public CatLoader(DbContext dbContext) {
            this.dbContext = dbContext;
        }

        public Cat[] Load() {
            var cats = this.dbContext.Query<Cat[]>().All();
            return cats;
        }
    }

