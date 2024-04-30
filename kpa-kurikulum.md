---
layout: page
title: Kurikulum
permalink: /kpa/kurikulum
---


### Kelas

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kelas</th>
      <th>Rentang Usia</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-kelas %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kelas }}</td>
      <td>{{ db.rentang-usia }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>

### Kurikulum

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kelas</th>
      <th>Mata Pelajaran</th>
      <th>Target Pembelajaran</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-kurikulum %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kelas }}</td>
      <td>{{ db.mata-pelajaran }}</td>
      <td>{{ db.target-pembelajaran }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>