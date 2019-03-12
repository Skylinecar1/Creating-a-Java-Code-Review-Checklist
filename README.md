# Creating-a-Java-Code-Review-Checklist
Group Activity


CheckPoints List Points -


1. File encoding: UTF-8

Source files are encoded in UTF-8.


2.  Whitespace characters.

All other whitespace characters in string and character literals are escaped.
Tab characters are not used for indentation.


3. File name

The source file name consists of the case-sensitive name of the top-level class it contains (of which there is exactly one), plus the .java extension.


4. Class declaration
 
Exactly one top-level class declaration

Each top-level class resides in a source file of its own.


5. Ordering of class contents

each class uses some logical order, which its maintainer could explain if asked. For example, new methods are not just habitually added to the end of the class, as that would yield "chronological by date added" ordering, which is not a logical ordering.

6. Braces are used where optional

Braces are used with if, else, for, do and while statements, even when the body is empty or contains only a single statement.


7. Nonempty blocks: K & R style

Braces follow the Kernighan and Ritchie style ("Egyptian brackets") for nonempty blocks and block-like constructs:
•No line break before the opening brace.
•Line break after the opening brace.
•Line break before the closing brace.
•Line break after the closing brace, only if that brace terminates a statement or terminates the body of a method, constructor, or named class. For example, there is no line break after the brace if it is followed by else or a comma.

eg -

return () -> {
  while (condition()) {
    method();
  }
};

return new MyClass() {
  @Override public void method() {
    if (condition()) {
      try {
        something();
      } catch (ProblemException e) {
        recover();
      }
    } else if (otherCondition()) {
      somethingElse();
    } else {
      lastThing();
    }
  }
};


8. Block indentation: +2 spaces

Each time a new block or block-like construct is opened, the indent increases by two spaces. When the block ends, the indent returns to the previous indent level

eg -

return () -> {
  while (condition()) {
    method();
  }
};

return new MyClass() {
  @Override public void method() {
    if (condition()) {
      try {
        something();
      } catch (ProblemException e) {
        recover();
      }
    } else if (otherCondition()) {
      somethingElse();
    } else {
      lastThing();
    }
  }
};


9. Indent continuation lines at least +4 spaces

When line-wrapping, each line after the first (each continuation line) is indented at least +4 from the original line.

When there are multiple continuation lines, indentation may be varied beyond +4 as desired. In general, two continuation lines use the same indentation level if and only if they begin with syntactically parallel elements


10. Comments

Block comment style

Block comments are indented at the same level as the surrounding code. They may be in /* ... */ style or // ... style. For multi-line /* ... */ comments, subsequent lines must start with * aligned with the * on the previous line.
/*
 * This is          // And so           /* Or you can
 * okay.            // is this.          * even do this. */
 */

