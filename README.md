# DistributionGo Classic

Windows 原生安裝版／Native Windows installer.

- [最新正式安裝檔 / Latest Setup](https://github.com/eltonwangpx-wq/distributiongo-classic/releases/latest/download/DistributionGo-Classic-Setup.exe)
- [版本與 SHA-256 / Releases and checksums](https://github.com/eltonwangpx-wq/distributiongo-classic/releases)
- [九語安裝說明 / Installation guide](docs/INSTALL.md)

只需下載 Setup EXE。支援 Windows 11 x64 24H2 以上，安裝時需要管理員批准。此版本未做程式碼簽章；請確認下載來源並核對 SHA-256。安裝時間依硬體而異，測試約 5～10 分鐘。

Download only the Setup EXE. Requires Windows 11 x64 24H2 or later and administrator approval. This version is unsigned; verify its source and SHA-256. Installation took about 5–10 minutes in testing.

新裝預設 `admin / distributiongo`，請登入後改密碼。預設倉庫 `0000 / default` 已包含 admin。更新或重裝接回不重設既有帳密。桌面及開始功能表提供 Web 捷徑；程式目錄的 `InstallationInfo.txt` 記錄網址、DB 位址及允許來源，不含密碼。

For new installations, sign in with `admin / distributiongo` and change the password. Warehouse `0000 / default` includes admin. Upgrades and reattachment retain existing credentials. Web shortcuts are on the desktop and Start menu. `InstallationInfo.txt` records endpoints and allowed sources without passwords.

LAN HTTPS uses a local CA. Confirm its fingerprint in Certificate trust and export before explicitly trusting it; each other computer needs one-time setup. Domain certificates may be imported as PFX. Certificate issuance and renewal are administrator-managed. ThousanAI uses a host-specific local key and requires privacy consent before cloud questions; no model API key is bundled.

Run Setup again to modify settings, upgrade, or reinstall using retained data. Uninstall removes the application and its services while keeping the data directory. Do not delete that directory to update the application.

## Backup and recovery (administrator PowerShell)

Backups briefly stop the owned DG services for consistency. They contain private keys and credentials: keep them protected and never attach them to public issues. Use a new local NTFS folder outside the program and data directories.

```powershell
& 'C:\Program Files\DistributionGo\installer\Native.Backup.ps1' -Operation Backup -Program 'C:\Program Files\DistributionGo' -Root 'C:\ProgramData\DistributionGo' -BackupPath 'D:\DG-Backups\before-update'
& 'C:\Program Files\DistributionGo\installer\Native.Backup.ps1' -Operation Verify -Program 'C:\Program Files\DistributionGo' -Root 'C:\ProgramData\DistributionGo' -BackupPath 'D:\DG-Backups\before-update'
& 'C:\Program Files\DistributionGo\installer\Native.Backup.ps1' -Operation Restore -Program 'C:\Program Files\DistributionGo' -Root 'C:\ProgramData\DistributionGo' -BackupPath 'D:\DG-Backups\before-update'
```

Restore requires the same host, role, paths and application package. Keep the matching installer. Web-only backups exclude the remote database, which must be backed up on its host. Upgrade recovery copies are stored under `C:\ProgramData\DistributionGoBackups`; previous restore state remains under the data folder's protected `recovery` directory. An administrator may archive obsolete recovery copies after acceptance.

備份／還原限相同主機、角色、路徑與應用包，請保留對應安裝檔。Web-only 的遠端 DB 必須另行備份。備份含私鑰與密碼，不可公開。升級備份及舊還原副本可在確認運作正常後由管理員封存清理。

## Third-party notices

The installer includes upstream license texts in `installer/notices`. Releases also provide a documentation/notices archive. PostgreSQL, Python, Caddy, WinSW, Python dependencies and Web libraries retain their respective licenses. This download repository does not publish the private DistributionGo development repository.

## Validation scope

Settings maintenance, upgrade, uninstall retaining data, reattachment and same-host backup/restore are covered by the release acceptance. Existing language and role evidence is retained. Remaining two-machine DB/Web, external Odoo and cross-computer CA acceptance are deferred; they are not represented as passed.