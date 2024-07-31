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
</tbody>
</table>

