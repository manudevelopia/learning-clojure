# Lesson 1

### 1. Install Leiningen

If you haven’t already, download and install Leiningen by following the instructions on the official website.

### 2. Create a New Project

Run the following command to create a new Leiningen project:

```lein new app my-first-clojure-project```

This will create a directory structure like this:

```
my-first-clojure-project/
├── README.md
├── project.clj
├── resources/
├── src/
│   └── my_first_clojure_project/
│       └── core.clj
├── test/
│   └── my_first_clojure_project/
│       └── core_test.clj
└── target/
```

### 3. Explore the Project Files

project.clj: Defines your project configuration, dependencies, and other settings.
src/my_first_clojure_project/core.clj: The main source file where you’ll write your code.
test/: A directory for writing unit tests.

### 4. Run the Default Application

Navigate into your project directory:

```cd my-first-clojure-project```

Run the application:

```lein run```

By default, it will print:

```Hello, World!```

### 5. Modify the Code

Open src/my_first_clojure_project/core.clj and customize the -main function. For example:

```clojure
(ns my-first-clojure-project.core
  (:gen-class))

(defn -main
  "A simple main function."
  [& args]
  (println "Welcome to my first Clojure project!"))
```

Run it again with lein run to see the updated message.

### 6. Add Dependencies

To add libraries, modify the :dependencies section in project.clj. For example:

```clojure
(defproject my-first-clojure-project "0.1.0-SNAPSHOT"
            :description "A simple Clojure project"
            :dependencies [[org.clojure/clojure "1.12.0"]]
            :main ^:skip-aot my-first-clojure-project.core
            :target-path "target/%s"
            :profiles {:uberjar {:aot :all}})
```

### 7. Next Steps

- Interactive Development: Use the REPL with lein repl.
- Testing: Add unit tests in the test folder.
- Feature Building: Start adding functionality like user input, data processing, or APIs.
