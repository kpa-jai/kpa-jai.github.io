---
layout: page
title: Materi
permalink: /kpa/materi
---

### Jenis Materi

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kode</th>
      <th>Nama Pelajaran</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-materi %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kode }}</td>
      <td>{{ db.nama-pelajaran }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>