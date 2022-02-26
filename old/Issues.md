# CodeIgniter4 まとめ

## 過去の問題
- v4.1.6
    - [Bug: ErrorException: Undefined index: file: SYSTEMPATH\Debug\Toolbar\Collectors\Database.php at line 142 #5539](https://github.com/codeigniter4/CodeIgniter4/issues/5539) ... 4.1.7 で修正済み
    - [Bug: Debug bar javascript issue with external script toggle #5541](https://github.com/codeigniter4/CodeIgniter4/issues/5541) ... 4.1.7 で修正済み
    - [Bug: BaseConnection::getConnectDuration() number_format(): Passing null to parameter #5535](https://github.com/codeigniter4/CodeIgniter4/issues/5535) ... 4.1.7 で修正済み
- [getCompiledSelect の罠、 useSoftDelete が抜け落ちる - Qiita](https://qiita.com/bananacoffee/items/0aff3f5cd005a5f1bfc6)
- Redis セッションのバグ
    - v4.1.4
    - v4.1.5 で修正済み
        - https://github.com/codeigniter4/CodeIgniter4/pull/5062
- [データベースセッションのバグ](https://github.com/codeigniter4/CodeIgniter4/issues/4807)
    - v4.1.2〜v4.1.4
    - v4.1.5 で修正済み
        - https://github.com/codeigniter4/CodeIgniter4/pull/4876
        - https://github.com/codeigniter4/CodeIgniter4/pull/5060
- 環境変数名にドットが使えない環境がある
    - 〜v4.1.4
    - v4.1.5 で対応済み
        - https://github.com/codeigniter4/CodeIgniter4/pull/5156
        - https://github.com/codeigniter4/CodeIgniter4/issues/4026
