

TM API vs Internal
==================

The TM Project tries to keep its public API as small as possible, and move all non-API classes and interfaces into packages marked as "internal".

What does it mean if a class is internal:
-----------------------------------------

Note that a class being in an "internal" package doesn't mean that nobody can ever use it. As per [Export-Package](https://github.com/eclipse-platform/eclipse.platform/blob/master/docs/Export-Package.md "Export-Package") also "internal" packages are exported, they are just tagged as discouraged access by an "x-internal:=true" specifier in the Manifest. The PDE Tools "Cleanup Manifest" wizard can do that automatically. So, if an interface is "internal", this just means that

*   We do not have to write documentation beyond the Javadoc
*   We do not have to guarantee binary compatibility over releases

Putting classes and interfaces in "internal" packages helps adopters focus on those interfaces that are public API. Sometimes, it will turn out that an idea for extending TM (which seemed to require "internal" access) can be solved in a better way by using public API interfaces only. Making stuff internal fosters discussions if people don't get what they think they need right away. These discussions are positive since they help to improve the real API.

Therefore, just because we think that "somebody could probably want to use that class" is not argument enough to make it API. We can design our code for extensibility even if the extensible classes are internal (they might be moved to public API at a later time).

What should become public API:
------------------------------

*   Classes and interfaces that are **documented in the current ISV docs**. I mean those architectural overviews and descriptions that go beyond the plain Javadoc - those that describe the core functionality of our frameworks and how to extend it.
*   Classes and interfaces that are **required by currently known products extending TM**, unless it turns out there is a better way of doing things.
*   Classes and interfaces that are **referenced by current API interfaces** as parameters, return values or superclasses ("extends" and "implements" clauses. In other words, this means that the API needs to be self-contained (which can actually be checked automatically by the Eclpse API Scanner from the WTP project).

All other classes and interfaces should be considered to be moved into "internal" packages.

It's better to have a small API that can be actually maintained with binary compatibility, than a larger API that needs to be changed later or forces us to make compromises we don't want to make.

Comments
--------


(Migrated from [https://wiki.eclipse.org/TM_API_vs_Internal](https://wiki.eclipse.org/TM_API_vs_Internal))