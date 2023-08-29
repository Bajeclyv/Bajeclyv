# Hello, I'm [@Fulbion](https://github.com/Fulbion) 👋

### main.cpp
```cpp
class Person
{
private:
    std::string m_username;
    int m_age;
    std::string m_country;
    std::string m_job;
    std::vector<std::string> m_languages;

public:
    Person(std::string username, int age, std::string country, std::string job, std::vector<std::string> languages):
    {
        this->m_username = username;
        this->m_age = age;
        this->m_country = country;
        this->m_job = job
        this->m_languages = languages;
    }

    void details()
    {
        std::cout << "Hello, my name's @" << m_username << ", I'm " << m_age << " and I come from " << m_country << ".\n";
        std::cout << "I'm currently a" << m_job << " and I'm coding in:\n";
        
        for (string l : m_languages)
        {
            std::cout << "* " << l << "\n";
        }
    }
};

int main()
{
    Person me("Fulbion", 16, "France", "student", { "C/C++", "Python", "JavaScript", "PHP" });
    me.details();
    return 0;
}
```

-----

## Output
```
Hello, my name's @Fulbion, I'm 16 and I come from France.
I'm currently a student and I'm coding in:
* C/C++
* Python
* JavaScript
* PHP
```
