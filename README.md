# Hello, I'm [@Fulbion](https://github.com/Fulbion) 👋

### Person.hpp
```cpp
#pragma once

#include <iostream>
#include <string>
#include <vector>
using namespace std; // Cursed line, it's just to make it clear :P

class Person
{
public:
    Person(string username, int age, string country, string job, vector<string> languages) :
        m_username(username), m_age(age), m_country(country), m_job(job), m_languages(languages)
    {
    }

    void details()
    {
        cout << "Hello, my name's @" << m_username << ", I'm " << m_age << " and I come from " << m_country << ".\n";
        cout << "I'm currently a" << m_job << " and I'm coding in:\n";
        
        for (string l : m_languages)
        {
            cout << "* " << l << "\n";
        }
    }

private:
    string m_username;
    int m_age;
    string m_country;
    string m_job;
    vector<std::string> m_languages;
};
```

### main.cpp
```cpp
#include "Person.hpp"

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
