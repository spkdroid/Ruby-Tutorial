# Ruby-Tutorial

Ruby Programming Language: A Versatile and Elegant Journey into Programming

# Ruby Programming Language

**1. History:**
   - Ruby was created by Yukihiro Matsumoto (often referred to as "Matz") in the mid-1990s in Japan.
   - It was designed to be a language that emphasizes simplicity and productivity, making it enjoyable for programmers to use.

**2. Key Features:**
   - **Object-Oriented:** Everything in Ruby is an object, which promotes a clean and consistent syntax.
   - **Dynamic Typing:** Ruby is dynamically typed, meaning you don't need to specify variable types.
   - **Garbage Collection:** Automatic memory management helps prevent memory leaks.
   - **Open Classes:** You can modify existing classes or add new methods to them during runtime.
   - **Metaprogramming:** Ruby allows for powerful metaprogramming, enabling code to modify itself.
   - **Blocks and Closures:** Blocks of code can be passed around as objects, facilitating elegant solutions to problems.

**3. Syntax:**
   - Ruby features a concise and readable syntax that prioritizes developer happiness.
   - It uses English-like keywords and often reads like plain English, which makes it accessible to beginners.

**4. Community and Ecosystem:**
   - Ruby has a vibrant and active community of developers who contribute to its growth and development.
   - The RubyGems package manager and the RubyGems.org repository make it easy to share and distribute Ruby libraries and gems.
   - Popular web frameworks like Ruby on Rails have made Ruby a preferred choice for web development.

**5. Use Cases:**
   - Ruby is versatile and can be used for various applications, including web development, scripting, automation, and more.
   - It is particularly well-known for its role in web development, thanks to the Ruby on Rails framework.

**6. Example:**
   ```ruby
   # A simple Ruby program
   class Greeter
     def initialize(name)
       @name = name
     end

     def greet
       puts "Hello, #{@name}!"
     end
   end

   greeter = Greeter.new("Alice")
   greeter.greet
   ```

**7. Learning Ruby:**
   - Ruby's simplicity and elegant syntax make it a great choice for beginners in programming.
   - You can start learning Ruby by installing it on your computer and working through tutorials, online courses, or books.

Ruby's philosophy of "optimizing for developer happiness" has made it a beloved language in the programming community, and it continues to be a popular choice for a wide range of software development projects. Whether you're a beginner or an experienced programmer, Ruby offers a friendly and enjoyable programming experience.

# Ruby Installation

**1. Installing Ruby on Linux:**

   - **Ubuntu/Debian:**
     ```bash
     sudo apt update
     sudo apt install ruby-full
     ```

   - **Fedora/RHEL:**
     ```bash
     sudo dnf install ruby
     ```

   - **Arch Linux:**
     ```bash
     sudo pacman -S ruby
     ```

**2. Installing Ruby on macOS:**

   - macOS typically comes with Ruby pre-installed. However, you can use a package manager like Homebrew to install a more up-to-date version of Ruby:
     ```bash
     brew install ruby
     ```

**3. Installing Ruby on Windows:**

   - You can use the RubyInstaller for Windows, which is a self-contained installer that includes Ruby, DevKit (for building native extensions), and the MSYS2 development toolchain.
     - Download the installer from [RubyInstaller](https://rubyinstaller.org/).
     - Follow the installation instructions provided on the website.

**4. Installing Ruby Using Version Managers:**

   - An alternative to installing Ruby directly is to use a version manager, which allows you to easily switch between different Ruby versions and manage gems. Two popular version managers for Ruby are RVM and rbenv.

     - **RVM (Ruby Version Manager):**
       ```bash
       # Install RVM
       \curl -sSL https://get.rvm.io | bash -s stable
       
       # Load RVM into the current shell session
       source ~/.rvm/scripts/rvm
       
       # Install Ruby
       rvm install ruby
       ```

     - **rbenv:**
       ```bash
       # Install rbenv
       git clone https://github.com/rbenv/rbenv.git ~/.rbenv
       echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
       echo 'eval "$(rbenv init -)"' >> ~/.bashrc
       source ~/.bashrc
       
       # Install Ruby-build as a plugin for rbenv
       git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
       
       # Install Ruby
       rbenv install ruby
       ```

These are general installation instructions, and the specific steps may vary depending on the version of Ruby you want to install and your system's configuration. Be sure to follow the official documentation and installation guides for your particular operating system and preferred installation method.

## Ruby Basics

1. **Hello, World!**
   ```ruby
   puts "Hello, World!"
   ```

2. **Variables and Data Types**
   ```ruby
   name = "John"
   age = 30
   height = 6.2
   is_student = true
   ```

3. **Conditionals (if-else)**
   ```ruby
   if age < 18
     puts "You're a minor."
   else
     puts "You're an adult."
   end
   ```

4. **Loops (while and for)**
   ```ruby
   # While loop
   i = 0
   while i < 5
     puts "Iteration #{i}"
     i += 1
   end

   # For loop
   for num in 1..3
     puts "Number #{num}"
   end
   ```

5. **Functions (Methods)**
   ```ruby
   def greet(name)
     puts "Hello, #{name}!"
   end

   greet("Alice")
   ```

6. **Arrays**
   ```ruby
   fruits = ["apple", "banana", "cherry"]
   puts fruits[0]  # Outputs "apple"
   fruits.push("orange")
   ```

7. **Hashes (Key-Value Pairs)**
   ```ruby
   person = {
     "name" => "John",
     "age" => 30,
     "city" => "New York"
   }

   puts person["age"]  # Outputs 30
   ```

8. **Object-Oriented Programming (OOP)**
   ```ruby
   class Dog
     def initialize(name, breed)
       @name = name
       @breed = breed
     end

     def bark
       puts "Woof! I'm #{@name}, the #{@breed}."
     end
   end

   dog1 = Dog.new("Buddy", "Golden Retriever")
   dog1.bark
   ```

9. **Input from User**
   ```ruby
   print "Enter your name: "
   user_name = gets.chomp
   puts "Hello, #{user_name}!"
   ```

10. **Exception Handling**
    ```ruby
    begin
      result = 10 / 0
    rescue ZeroDivisionError
      puts "Error: Division by zero."
    end
    ```

11. **String Manipulation**
    ```ruby
    text = "Ruby is a great language!"
    puts text.downcase
    puts text.capitalize
    puts text.gsub("great", "wonderful")
    ```

12. **Iterating Through Arrays**
    ```ruby
    numbers = [1, 2, 3, 4, 5]
    sum = 0

    numbers.each do |num|
      sum += num
    end

    puts "The sum of numbers is: #{sum}"
    ```

13. **Symbols**
    ```ruby
    # Using symbols as keys in a hash
    person = {
      name: "Alice",
      age: 25,
      city: "London"
    }

    puts person[:name]
    ```

14. **Class Inheritance**
    ```ruby
    class Cat < Animal
      def speak
        puts "Meow!"
      end
    end

    cat = Cat.new
    cat.speak
    ```

15. **Modules and Mixins**
    ```ruby
    module Flyer
      def fly
        puts "I can fly."
      end
    end

    class Bird
      include Flyer
    end

    bird = Bird.new
    bird.fly
    ```

16. **File I/O**
    ```ruby
    # Writing multiple lines to a file
    File.open("multiline.txt", "w") do |file|
      file.puts("Line 1")
      file.puts("Line 2")
      file.puts("Line 3")
    end

    # Reading lines from a file
    File.open("multiline.txt", "r") do |file|
      file.each_line do |line|
        puts line
      end
    end
    ```

17. **Regular Expressions**
    ```ruby
    # Extracting email addresses from a text
    text = "Email me at user1@example.com or user2@gmail.com"
    emails = text.scan(/\b[\w+\-.]+@[a-z\d\-]+(\.[a-z\d\-]+)*\.[a-z]+\b/i)
    puts "Found emails: #{emails}"
    ```

18. **Using Gems**
    ```ruby
    require 'httparty'

    response = HTTParty.get("https://jsonplaceholder.typicode.com/posts/1")
    if response.success?
      data = JSON.parse(response.body)
      puts "Title: #{data['title']}"
      puts "Body: #{data['body']}"
    else
      puts "Failed to fetch data."
    end
    ```

Feel free to run and modify these examples to deepen your understanding of Ruby programming.

## Advanced Ruby

**1. Metaprogramming:**

   Metaprogramming is the ability of a programming language to write, modify, or manipulate its own code during runtime. In Ruby, metaprogramming allows you to define or modify classes, methods, and their behavior dynamically. It is achieved using techniques like `eval`, `define_method`, and reflection.

   ```ruby
   class MyClass
     define_method :dynamic_method do
       puts "This method was defined dynamically."
     end
   end

   obj = MyClass.new
   obj.dynamic_method
   ```

   In this example, the `define_method` method is used to define `dynamic_method` dynamically within the `MyClass` class.

**2. Closures and Blocks:**

   Closures are functions or blocks of code that can be passed around as first-class objects. In Ruby, blocks are a form of closures and are commonly used with methods that yield control to a block of code.

   ```ruby
   def perform_operation(x, y, &block)
     result = block.call(x, y)
     puts "Result: #{result}"
   end

   perform_operation(5, 3) { |a, b| a + b }
   ```

   In this example, the `&block` parameter allows us to pass a block of code to the `perform_operation` method. Inside the method, `block.call(x, y)` executes the provided block with the given arguments.

**3. Modules and Mixins:**

   Modules in Ruby are a way to encapsulate methods, constants, and classes. They can be included in classes using the `include` keyword, allowing classes to inherit module methods. This is known as a mixin.

   ```ruby
   module Greetings
     def say_hello
       puts "Hello!"
     end
   end

   class Person
     include Greetings
   end

   person = Person.new
   person.say_hello
   ```

   The `Person` class includes the `Greetings` module, giving instances of `Person` access to the `say_hello` method defined in the module.

**4. Procs and Lambdas:**

   Procs and lambdas are objects that represent blocks of code. They can be stored in variables and passed as arguments to methods. Lambdas are similar to Procs but have stricter argument checking.

   ```ruby
   add = Proc.new { |a, b| a + b }
   result = add.call(2, 3)
   puts "Result: #{result}"
   ```

   In this example, a Proc called `add` is defined to perform addition. The `call` method is used to execute the code block stored in the Proc.

**5. Method Missing:**

   Ruby's `method_missing` method allows you to intercept and handle calls to undefined methods in an object. This can be used for dynamic method dispatch or creating flexible APIs.

   ```ruby
   class DynamicMethod
     def method_missing(name, *args)
       puts "You called the method '#{name}' with arguments #{args}."
     end
   end

   obj = DynamicMethod.new
   obj.some_undefined_method("arg1", "arg2")
   ```

   When `some_undefined_method` is called on `obj`, the `method_missing` method is invoked, and it prints a message indicating the method name and arguments.

**6. Operator Overloading:**

   Operator overloading in Ruby allows you to redefine or customize the behavior of operators for your custom classes. This enables you to create more expressive code for specific data types.

   ```ruby
   class ComplexNumber
     attr_reader :real, :imaginary

     def initialize(real, imaginary)
       @real = real
       @imaginary = imaginary
     end

     def +(other)
       ComplexNumber.new(@real + other.real, @imaginary + other.imaginary)
     end
   end

   num1 = ComplexNumber.new(3, 2)
   num2 = ComplexNumber.new(1, 5)
   result = num1 + num2
   puts "Result: #{result.real} + #{result.imaginary}i"
   ```

   In this example, we define a `ComplexNumber` class and overload the `+` operator to perform addition of complex numbers in a more natural way.

These advanced Ruby concepts provide developers with powerful tools for creating dynamic, flexible, and expressive code in a variety of situations. Understanding and using these features effectively can significantly enhance your Ruby programming skills.
