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

### Daftar Materi Web dan Dokumen

{% assign sorted_kurikulum = site.data.db-materi-kelas | sort: 'kelas' %}

<table>
  <thead>
    <tr>
      <!-- <th>No.</th> -->
      <th>Kelas</th>
      <th>Nama Pelajaran</th>
      <th>Link Web</th>
      <th>Link Doc</th>
    </tr>
  </thead>
  <tbody>
  {% for db in sorted_kurikulum %}
    <tr>
      <!-- <td>{{ db.no }}</td> -->
      <td>{{ db.kelas }}</td>
      <td>{{ db.mata-pelajaran }}</td>
      <td><a href="{{ db.link-materi-web }}" target="_blank">Web</a></td>
      <td><a href="{{ db.link-materi-dokumen }}" target="_blank">Doc</a></td>
    </tr>
  {% endfor %}  
  </tbody>
</table>