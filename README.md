# Hello, I'm [@Fulbion](https://github.com/Fulbion) 👋

## Person.hpp
```cpp
#pragma once

#include <iostream>
#include <string>
#include <vector>

class Person
{
public:
    Person();
    Person(const std::string& i_username, const int i_age, const std::string& i_country, const std::string& i_job, const std::vector<std::string>& i_languages);

    void details();

private:
    std::string m_username;
    int m_age;
    std::string m_country;
    std::string m_job;
    std::vector<std::string> m_languages;
};
```

## Person.cpp
```cpp
#include "Person.hpp"

Person::Person(const std::string& i_username, const int i_age, const std::string& i_country, const std::string& i_job, const std::vector<std::string>& i_languages) :
    m_username(i_username), m_age(i_age), m_country(i_country), m_job(i_job), m_languages(i_languages)
{
}

void Person::details()
{
    std::cout << "Hello, my name's @" << m_username << ", I'm " << m_age << " and I come from " << m_country << ".\n";
    std::cout << "I'm currently a << m_job << " and I'm coding in:\n";

    for (std::string l : m_languages)
    {
        std::cout << "* " << l << "\n";
    }
}
```

## main.cpp
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
