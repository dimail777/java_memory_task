# Java spaces

### Heap, Stack, String pool, etc

        public class PersonService {

          public PersonEntity create(Integer age, String name) {
            if (name == null) {
              name = "unknown";                                   // link's space, value's space
            }
            if (age == null) {
              age = 0;                                            // link's space, value's space
            }

            PersonEntity person = new PersonEntity();             // link's space, value's space
            person.setAge(age);
            person.setName(name);

            return person;
          }
        }

        public class PersonEntity {

          private int age;                                        // link's space, value's space
          private String name;                                    // link's space, value's space

          public void setAge(int age) {
            this.age = age;
          }

          public void setName(String name) {
            this.name = name;
          }

          public int getAge() {
            return age;
          }

          public String getName() {
            return name;
          }
        }
