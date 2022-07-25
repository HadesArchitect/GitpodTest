<div class="top">

# Try It Out: Cassandra Query Language (CQL)
### [◂](command:katapod.loadPage?intro){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step2){.steps}
</div>

# Connect

First things first, we have to connect to the database. For that we will use a console client called `cqlsh` (Cassandra Query Language Shell). For the locally installed Cassandra with default settings we can connect as simple as that:

```
cqlsh
```

# Create a keyspace

Let's first start learning CQL by creating a keyspace, using the `CREATE KEYSPACE` command.

```
CREATE KEYSPACE demo WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};
```

*ProTip:* You can use the `Tab` key in `cqlsh` to auto-complete or suggest the next part of your command, as you type.

A keyspace is a way to logically group a collection of database objects together, such as:

* tables
* user-defined types
* user-defined functions
* and more!

This is similar concept to the `database` or `namespace` used in relational databases.

In addition, the keyspace also controls the replication behavior for all of the data stored in the keyspace.

---

## Take a quick quiz to check your knowledge!

<!-- Quiz Results -->
<div id="quiz-result" class="card">
    You Scored <span id="quiz-percent"></span>% - <span id="quiz-score"></span>/<span id="quiz-max-score"></span><br/>
</div>

<!-- Quiz Container -->
<div id="quiz">
    <!-- Question 1 -->
    <div class="card quizlib-question">
        <div class="quizlib-question-title">1. Which console tool we use to connect to the database?</div>
        <div class="quizlib-question-answers">
            <ul>
                <li><label><input type="radio" name="q1" value="sqlsh"> sqlsh</label></li>
                <li><label><input type="radio" name="q1" value="cqlsh"> cqlsh</label></li>
                <li><label><input type="radio" name="q1" value="bash"> bash</label></li>
            </ul>
        </div>
    </div>
    <!-- Question 2 -->
    <div class="card quizlib-question">
        <div class="quizlib-question-title">2. In Cassandra, a logical group of tables called a ...?</div>
        <div class="quizlib-question-answers">
            <input type="text" name="q2">
        </div>
    </div>
    <!-- Question 3 -->
    <div class="card quizlib-question">
        <div class="quizlib-question-title">3. Which objects a keyspace can group together?</div>
        <div class="quizlib-question-answers">
            <ul>
                <li><label><input type="checkbox" name="q3" value="a"> Cassandra Servers</label></li>
                <li><label><input type="checkbox" name="q3" value="b"> Tables</label></li>
                <li><label><input type="checkbox" name="q3" value="c"> User-Defined Types</label></li>
                <li><label><input type="checkbox" name="q3" value="d"> User-Defined Functions</label></li>
            </ul>
        </div>
    </div>
    <!-- Answer Button -->
    <button type="button" onclick="showResults();">Submit Answer</button>
</div>

<!-- ---

*Great, you now know how to create a keyspace in Apache Cassandra!* -->

<style>
    a.disabled {
        pointer-events: none;
        cursor: wait !important;
        background-color: grey;
    }
</style>

[Answer quiz questions to continue](command:katapod.loadPage?step2){.orange_bar .disabled #continue}

<script>
window.onload = function() {
    quiz = new Quiz('quiz', [
        'cqlsh',
        'keyspace',
        ['b', 'c', 'd']
    ]);
};
</script>