# Tiny-TID
A basic Form of the TID-Language, a language for E2E tests.

This Project shows how the TID Language could be used.

    PRECONDIDTION:openFinancialLogin
    ACTION:WAITFOR
    Applications.Financial.Login.Username|true
    Applications.Financial.Login.Password|true
    Applications.Financial.Login.ButtonLogin|true
    ACTION:CHECKENABLED
    Applications.Financial.Login.Username|true
    Applications.Financial.Login.Password|true
    Applications.Financial.Login.ButtonLogin|false
    ACTION:SETVALUE
    Applications.Financial.Login.Username|user
    Applications.Financial.Login.Password|password
    ACTION:CHECKENABLED
    Applications.Financial.Login.ButtonLogin|true
    ACTION:CLICK
    Applications.Financial.Login.ButtonLogin|click
    ACTION:WAITFOR
    Applications.Financial.Login.Username|false
    Applications.Financial.Login.Password|false
    Applications.Financial.Login.ButtonLogin|false
    ACTION:CHECKVALUE
    Applications.Financial.Username|user
    ROUTINE:ApplicationFinancialLogout


TID stands for Test Input Data.

The idea based on a job, where I should implement testautomation for the testing department, but the situation was special.

- the testers had mainly user knowledge of computers
- the domain was very special, so I expected to get to need about one and a half year to get the knowledge to write tests that make sense
- to see  the complexitiy: in the software there where about 40 different areas with in total about 1600 masks with about 10 Fields each, a simple complete domain testcase would use about 15 masks. More complex testcases going over different areas.
- there were about 5 testers, whith excelent domain knowledege an one automation specialist (me)
- the chief of the department needed success, cause the former automation projects had crashed, because even the simplest testing tools would need technical knowledege to get the tests right in this domain

The only way to manage the situation, was to get the testers on board to get the writing the automated tests with their domain knowledge. 
The tests had to be easy to write, read, execute and adapted.

The ideas was born to write a simple not clumpsy nor turing afine domain language that hides all the technial stuff.
All technical stuff would be mine, all domain testing would go to the testers.
The company would win one and a half year, because I would not use time to get domain knowledge.



