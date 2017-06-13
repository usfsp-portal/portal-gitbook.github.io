S
ite Roles
The system uses roles to manage user capabilities.

A role combines at least two and sometimes three components: role, scope and target.

Role is a numeric ranking from '0' to '10'. Higher-ranking role values represent more extensive capabilities. A role of '10' can do anything; a role of '0' can do very little.

Roles exist within a context defined by the role's scope. Six scopes are possible:

unit (1)
chat (2)
user (3)
reports (4)
bot (5)
site (6)
Higher-ranking roles have additional capabilities regardless of their scope, but the particulars vary from one scope to the next. For example, a role of '10' on a unit would entail the ability to manage the users who belong to the unit, whereas a role of '10' on a user would entail the ability to edit the contact information for the user.

For the first five scopes, a target must be defined. The target is the specific entity to which the privileges are to be applied. So, for example, if a role is set on the 'user' scope, a target ID (in this case user ID) must also be set. If no target ID is set, privileges will be granted across all entities, in this case, all users. For example, the following entry would give the User with ID 34 the ability to edit any content on their own user page:

id_user: 34
role: 10
scope: 3
target: 34
On the other hand, the following entry would give the same user the ability to edit any content on ANY user:

id_user: 34
role: 10
scope: 3
target:
The scope of site is special in that it provides global privileges to a user.

In general, the OSSP role system eschews hierarchy in favor of giving the right people the right capabilities in the right contexts, regardless of organizational structures.

Role 0. Ghost users -- those who have not logged into an official account -- are typically assigned to this role.
Role 1. Regular/student users are typically assigned to this role.
Role 5. Support staff are typically assigned to this role.
Role 10. Routers are typically assigned to this role.
