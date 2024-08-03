# Database design

***

## Project

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr>
<td>project_id</td>
<td>bigint</td>
<td>PK</td>
</tr>
<tr>
<td>project_name</td>
<td>varchar</td>
<td>not null</td>
</tr>
<tr>
<td>project_start_date</td>
<td>timestamp</td>
<td>not null</td>
</tr>
<tr><td>project_status</td><td>varchar</td><td>not null</td></tr>
<tr><td>project_description</td><td>varchar</td><td>not null</td></tr>
</tbody>
</table>

## Task
<table>
<thead><th>
Column
</th>
<th>
Type
</th>
<th>
Constraints
</th></thead>
<tbody>
<tr><td>task_id</td><td>bigint</td><td>PK</td></tr>
<tr><td>task_name</td><td>varchar</td><td>not null</td></tr>
<tr><td>task_status</td><td>varchar</td><td>not null</td></tr>
<tr><td>project_id</td><td>bigint</td><td>FK Project (project_id)</td></tr>
<tr><td>start_date</td><td>timestamp</td><td>not null</td></tr>
<tr><td>end_date</td><td>timestamp</td><td>not null</td></tr>
<tr><td>created_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>last_modified_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_on</td><td>timestamp</td><td>not null</td></tr>
</tbody>
</table>

## Team

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr>
<td>team_id</td>
<td>bigint</td>
<td>PK</td>
</tr>
<tr>
<td>team_name</td>
<td>varchar</td>
<td>not null</td>
</tr>
<tr><td>created_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>owner</td><td>varchar</td><td>not null</td></tr>
<tr><td>description</td><td>varchar</td><td>not null</td></tr>
</tbody>
</table>

## User

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr><td>user_id</td><td>bigint</td><td>PK</td></tr>
<tr><td>first_name</td><td>varchar</td><td>not null</td></tr>
<tr><td>last_name</td><td>varchar</td><td>not null</td></tr>
<tr><td>password_hash</td><td>varchar</td><td>not null</td></tr>
<tr><td>email</td><td>varchar</td><td>not null</td></tr>
<tr><td>phone</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_by</td><td>varchar</td><td>not null</td></tr>
</tbody>
</table>

## User Team Mapping

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr><td>user_id</td><td>bigint</td><td>PK</td></tr>
<tr><td>team_id</td><td>varchar</td><td>not null</td></tr>
<tr><td>added_on</td><td>timestamp</td><td>not null</td></tr>
</tbody>
</table>

## Project Template

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr><td>template_id</td><td>bigint</td><td>PK</td></tr>
<tr><td>project_description</td><td>varchar</td><td>not null</td></tr>
<tr><td>type</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_by</td><td>varchar</td><td>not null</td></tr>
</tbody>
</table>

## Comments

<table>
<thead>
<th>Column</th>
<th>Type</th>
<th>Constraints</th>
</thead>
<tbody>
<tr><td>comment_id</td><td>bigint</td><td>PK</td></tr>
<tr><td>comment</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>created_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_on</td><td>timestamp</td><td>not null</td></tr>
<tr><td>last_modified_by</td><td>varchar</td><td>not null</td></tr>
<tr><td>parent_comment</td><td>bigint</td><td>FK Comment(comment_id)</td></tr>
</tbody>
</table>

