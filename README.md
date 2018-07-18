# Laravel-Many-to-Many-Eloquent-Relationship

+ Retrieve Records:

$user = User::find(1);	
dd($user->roles);

$role = Role::find(1);	
dd($role->users);

---------------------------------------------

+ Create Records:

$user = User::find(2);	
$roleIds = [1, 2];
$user->roles()->attach($roleIds);

$user = User::find(3);	 
$roleIds = [1, 2];
$user->roles()->sync($roleIds);

$role = Role::find(1);	
$userIds = [10, 11];
$role->users()->attach($userIds);

---------------------------------------------

+ update Recode:

$role = Role::find(2);	
$userIds = [10, 11];
$role->users()->sync($userIds);

