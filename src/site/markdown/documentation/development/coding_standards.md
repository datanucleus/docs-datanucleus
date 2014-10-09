<head><title>Coding Standards</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## Coding Standards

Here we provide an overview of the coding standards employed in DataNucleus.
__If you want to work on DataNucleus or contribute code to DataNucleus you are expected to use these coding standards. 
We know everyone has their own preference but these are ours so you follow them or any contributed code will not be 
directly included as is__.
They may differ from Oracle's coding conventions but then those are the conventions of some US company and that doesn't 
mean that they are necessarily "the best", "the official" or any such title. These are ours, so best get used to it ;-).

* __Indentation__ : 4 characters indent
* __Tabs__ : no tabs please!
* __Braces__ : insert a new line before opening brace and a new line before closing brace. Opening and closing braces should line up vertically.
* __Line Length__ : max line length 140
* __Imports__ : fully specify imports. Do NOT use asterisk notation!
* __Java Language Level__ : write for JDK1.7 as a minimum. Anything that requires Java 1.8 should go in the <i>datanucleus-java8</i> plugin. The test suite can use Java 1.8 code.
* __Fields positioning__ : place fields at the top of a class.
* __Logging__ : use _org.datanucleus.util.NucleusLogger_ which wraps Log4j, java.util.logging etc. Log as much info as is considered necessary at the appropriate level.
See [org.datanucleus.util.NucleusLogger](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/util/NucleusLogger.html) for details
* __Localisation__ : all output exception and log messages should be localised. 
See [org.datanucleus.util.Localiser](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/util/Localiser.html) for details
* __Licensing__ : make sure you include the [standard DataNucleus/Apache 2 license copyright header](#Licensing) to all files


If you are using Eclipse then we have an [XML Configuration](code-conventions-eclipse.xml) to specify in Eclipse.

### Examples

Example of brace policy and other things

	package mypackage;

	import java.util.LinkedList;

	public class MyIntStack
	{
	    private final LinkedList fStack;
	
	    public MyIntStack()
	    {
	        fStack = new LinkedList();
	    }
	
	    public int pop()
	    {
	        return ((Integer) fStack.removeFirst()).intValue();
	    }
	
	    public void push(int elem)
	    {
	        fStack.addFirst(new Integer(elem));
	    }
	
	    public boolean isEmpty()
	    {
	        return fStack.isEmpty();
	    }
	}

Example of indentation

	class Example
	{
	    int[] myArray = {1, 2, 3, 4, 5, 6};
	    int theInt = 1;
	    String someString = "Hello";
	    double aDouble = 3.0;
	
	    void foo(int a, int b, int c, int d, int e, int f)
	    {
	        switch (a)
	        {
	            case 0 :
	                Other.doFoo();
	                break;
	            default :
	                Other.doBaz();
	        }
	    }
	
	    void bar(List v)
	    {
	        for (int i = 0; i &lt; 10; i++)
	        {
	            v.add(new Integer(i));
	        }
	    }
	}

Example with if ... else

	class Example
	{
	    void bar()
	    {
	        do
	        {
	        }
	        while (true);
	        try
	        {
	        }
	        catch (Exception e)
	        {
	        }
	    }

	    void foo2()
	    {
	        if (true)
	        {
	            return;
	        }
	        if (true)
	        {
	            return;
	        }
	        else if (false)
	        {
	            return;
	        }
	        else
	        {
	            return;
	        }
	    }

	    void foo(int state)
	    {
	        if (true)
	        {
	            return;
	        }
	        if (true)
	        {
	            return;
	        }
	        else if (false)
	        {
	            return;
	        }
	        else
	        {
	            return;
	        }
	    }
	}

## Licensing

All contributions to the DataNucleus Project must adhere to the Apache 2 license. Notwithstanding the above, at the discretion of the PMC, 
DataNucleus Project downloads may include separately licensed code from third parties as a convenience and where permitted by the third party license, 
provided this is clearly indicated.

All contributions must contain the following copyright notice.

	/**********************************************************************
	Copyright (c) 2006 {your name} and others. All rights reserved.
	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at
	
	    http://www.apache.org/licenses/LICENSE-2.0
	
	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.
	
	Contributors:
	{year} {contributor1} - {description of contribution}
	{year} {contributor2} - {description of contribution}
	    ...
	**********************************************************************/


## References

In this document we describe just a small set of guidelines. Some references are really worth a read, though our particular guidelines above override some of the things here.

* [Java Code Conventions](http://www.oracle.com/technetwork/java/javase/documentation/codeconvtoc-136057.html)
* [How to write doc comments for Javadoc](http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html)
* [How to write unmaintainable code (what not to do)](http://mindprod.com/jgloss/unmain.html)
* [Scott Ambler Programming Guidelines](http://www.ambysoft.com/essays/codingGuidelines.html)
