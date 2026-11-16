# Git Contribution Guidelines

Dokumen ini berisi standar penggunaan Git pada repository `git-standard-practice` agar pengelolaan perubahan kode lebih terstruktur, konsisten, dan mudah dipahami.

## 1. Branch Naming Convention

Setiap branch harus menggunakan format:

`<type>/<short-description>`

Jenis branch yang digunakan:

| Prefix | Kegunaan | Contoh |
|---|---|---|
| `feature/` | Menambahkan fitur baru | `feature/user-login` |
| `fix/` | Memperbaiki bug | `fix/login-error` |
| `docs/` | Mengubah dokumentasi | `docs/update-readme` |
| `refactor/` | Merapikan struktur kode | `refactor/auth-service` |
| `test/` | Menambahkan atau memperbaiki pengujian | `test/login-validation` |
| `chore/` | Pemeliharaan proyek | `chore/update-dependencies` |

Aturan penamaan:
- Menggunakan huruf kecil.
- Menggunakan tanda hubung (`-`) sebagai pemisah kata.
- Nama branch harus singkat dan menggambarkan perubahan.

## 2. Commit Message Convention

Setiap commit harus mengikuti format Conventional Commits:

`<type>(<scope>): <subject>`

Jenis commit yang digunakan:

| Type | Kegunaan |
|---|---|
| `feat` | Menambahkan fitur baru |
| `fix` | Memperbaiki bug |
| `docs` | Mengubah dokumentasi |
| `style` | Mengubah format kode tanpa mengubah logika |
| `refactor` | Merapikan struktur kode |
| `test` | Menambahkan atau memperbaiki pengujian |
| `chore` | Pemeliharaan proyek |

Contoh commit yang benar:
- `feat(auth): add login feature`
- `fix(auth): resolve login validation error`
- `docs(readme): update installation guide`
- `chore(project): update dependencies`

Aturan penulisan:
- Menggunakan huruf kecil pada subject.
- Tidak menggunakan titik di akhir subject.
- Menggunakan kalimat singkat dan jelas.
- Menjelaskan perubahan yang dilakukan.

## 3. Pull Request Convention

Setiap perubahan yang dibuat melalui branch terpisah harus diajukan melalui Pull Request sebelum digabungkan ke branch `main`.

Aturan Pull Request:
- Judul PR mengikuti format Conventional Commits.
- Satu PR hanya membahas satu tujuan perubahan.
- Deskripsi harus menjelaskan perubahan yang dilakukan.
- Perubahan harus diperiksa kembali sebelum di-merge.
- Pastikan tidak ada konflik dengan branch `main`.

Template deskripsi Pull Request:

### Description
Jelaskan tujuan perubahan.

### Changes
- Daftar perubahan yang dilakukan.

### Checklist
- [ ] Kode sudah diperiksa.
- [ ] Perubahan sudah diuji.
- [ ] Tidak ada file sensitif yang ikut diunggah.
- [ ] Tidak ada konflik dengan branch `main`.

Karena repository dikelola secara individu, pemeriksaan kode dilakukan secara mandiri sebelum Pull Request di-merge.

## 4. General Git Workflow

Alur kerja Git yang digunakan:

1. Memastikan branch `main` sudah diperbarui.
2. Membuat branch baru sesuai jenis pekerjaan.
3. Melakukan perubahan kode.
4. Menyimpan perubahan menggunakan commit sesuai Conventional Commits.
5. Mengunggah branch ke GitHub.
6. Membuat Pull Request.
7. Memeriksa perubahan dan melakukan merge ke `main`.
8. Menghapus branch yang sudah selesai digunakan.
