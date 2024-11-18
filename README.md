# Rust - პროგრამირების ენა

![Build Status](https://github.com/rust-lang/book/workflows/CI/badge.svg)

ეს რეპოზიტორია შეიცავს "Rust პროგრამირების ენა" წიგნის წყაროს.

[წიგნი ხელმისაწვდომია ბეჭდური ფორმატით No Starch Press-დან][nostarch].

[nostarch]: https://nostarch.com/rust-programming-language-2nd-edition

თქვენ ასევე შეგიძლიათ წაიკითხოთ წიგნი ონლაინ, სრულიად უფასოდ. იხილეთ წიგნი, უახლესი გამოშვებებით: [stable], [beta], [nightly]. გაითვალისწინეთ, რომ ამ ვერსიებში არსებული პრობლემები შესაძლოა უკვე გამოსწორებული იყოს ამ რეპოზიტორიაში, რადგან ეს ვერსიები ნაკლებად ხშირად
განახლდება.

[stable]: https://doc.rust-lang.org/stable/book/
[beta]: https://doc.rust-lang.org/beta/book/
[nightly]: https://doc.rust-lang.org/nightly/book/

იხილეთ [გამოშვებები], რათა გადმოწეროთ ყველა კოდის ჩამონათვალი, რომელიც წიგნშია წარმოდგენილი.

[გამოშვებები]: https://github.com/rust-lang/book/releases

## მოთხოვნები

წიგნის ასაგებად საჭიროა [mdBook], სასურველია ის ვერსია, რომელსაც rust-lang/rust იყენებს [ამ ფაილში][rust-mdbook]. მის მისაღებად:

[mdBook]: https://github.com/rust-lang/mdBook
[rust-mdbook]: https://github.com/rust-lang/rust/blob/master/src/tools/rustbook/Cargo.toml

```bash
$ cargo install mdbook --locked --version <version_num>
```

წიგნი ასევე იყენებს ორ mdBook-ის დანამატს( plugins ), რომლებიც ამ რეპოზიტორიის ნაწილია. წიგნის აგების პროცესში გაფრთხილებები გამოჩნდება, და საბოლოო შედეგი სრულყოფილად არ იქნება, მაგრამ მაინც შეძლებთ წიგნის აგებას. დანამატების გამოსაყენებლად, უნდა გაუშვათ შემდეგი კოდი:

```bash
$ cargo install --locked --path packages/mdbook-trpl-listing
$ cargo install --locked --path packages/mdbook-trpl-note
```

## აგება

წიგნის ასაგებად აკრიფეთ:

```bash
$ mdbook build
```

შედეგი შეინახება `book` ქვეფოლდერში. მის სანახავად გახსენით იგი თქვენს ვებ ბრაუზერში.

_Firefox:_

```bash
$ firefox book/index.html                       # Linux
$ open -a "Firefox" book/index.html             # OS X
$ Start-Process "firefox.exe" .\book\index.html # Windows (PowerShell)
$ start firefox.exe .\book\index.html           # Windows (Cmd)
```

_Chrome:_

```bash
$ google-chrome book/index.html                 # Linux
$ open -a "Google Chrome" book/index.html       # OS X
$ Start-Process "chrome.exe" .\book\index.html  # Windows (PowerShell)
$ start chrome.exe .\book\index.html            # Windows (Cmd)
```

ტესტების გასაშვებად:

```bash
$ cd packages/trpl
$ mdbook test --library-path packages/trpl/target/debug/deps
```

## კონტრიბუცია:

ჩვენთვის დიდი პატივი იქნება თქვენი დახმარება! თუ გაინტერესებთ, რა სახის კონტრიბუციას ვსაჭიროებთ, იხილეთ [CONTRIBUTING.md][contrib].

[contrib]: https://github.com/rust-lang/book/blob/main/CONTRIBUTING.md

რადგან წიგნი [ბეჭდური ფორმატითაც][nostarch]ხელმისაწვდომია და გვსურს, რომ ონლაინ ვერსია რაც შეიძლება ახლოს იყოს ბეჭდურ ვერსიასთან, შესაძლოა მეტი დრო დაგვჭირდეს თქვენი საკითხის ან pull request-ის განხილვისთვის, ვიდრე ამას მოელით.

აქამდე, ვმუშაობდით უფრო მასშტაბურ რევიზიებზე [Rust Editions](https://doc.rust-lang.org/edition-guide/) გამოშვებებთან ერთად. ამ დიდ რევიზიებს შორის ვასწორებთ მხოლოდ შეცდომებს. თუ თქვენი საკითხი ან pull request პირდაპირ შეცდომის გამოსწორებას არ ეხება, შესაძლოა ის დაელოდოს მომდევნო მასშტაბურ რევიზიას: ეს პროცესი შესაძლოა თვის ან წლის ფარგლებშიც მოიცავდეს. მადლობა მოთმინებისთვის!

### თარგმანები

ჩვენ მოხარულები ვიქნებით, თუ დაგვეხმარებით წიგნის თარგმნაში! იხილეთ [Translations] ლეიბლი, რათა შეუერთდეთ მიმდინარე ძალისხმევას. გახსენით ახალი საკითხი, რათა დაიწყოთ მუშაობა ახალ ენაზე! ჩვენ ველოდებით [mdbook support] მრავალი ენისათვის, სანამ რომელიმე მათგანს დავამატებთ, თუმცა თავისუფლად დაიწყეთ!

[Translations]: https://github.com/rust-lang/book/issues?q=is%3Aopen+is%3Aissue+label%3ATranslations
[mdbook support]: https://github.com/rust-lang/mdBook/issues/5

## მართლწერის შემოწმება

წყაროს ფაილების მართლწერის შეცდომებზე სკანირებისათვის შეგიძლიათ გამოიყენოთ `spellcheck.sh` სკრიპტი, რომელიც ხელმისაწვდომია `ci` დირექტორიაში. მას სჭირდება ვალიდური სიტყვების ლექსიკონი, რომელიც მოწოდებულია `ci/dictionary.txt` ფაილში.

თუ სკრიპტი ცრუ დადებით შედეგს დააბრუნებს (მაგალითად, თქვენ გამოიყენეთ სიტყვა `BTreeMap`, რომელიც სკრიპტმა არასწორად მიიჩნია), უნდა დაამატოთ ეს სიტყვა `ci/dictionary.txt`-ში (შეინარჩუნეთ დალაგებული თანმიმდევრობა კონსისტენტურობისთვის).
