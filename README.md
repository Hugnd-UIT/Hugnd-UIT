<div align="center">

<img src="./logo.gif" alt="Nguyễn Duy Hưng - Agentic security dev" width="560" />

<br />

<img src="https://img.shields.io/badge/UIT-University%20of%20Information%20Technology-0a7ea4?style=flat" alt="UIT" />
<img src="https://img.shields.io/badge/Focus-AI%20Security-16a34a?style=flat" alt="AI Security" />
<img src="https://img.shields.io/badge/Role-Bug%20Hunter-dc2626?style=flat" alt="Bug Hunter" />
<img src="https://img.shields.io/badge/Field-Vuln%20Research-ea580c?style=flat" alt="Vulnerability Research" />
<img src="https://img.shields.io/badge/Field-Academic%20Research-7c3aed?style=flat" alt="Academic Research" />
</div>

---

## About me

Hi, I'm **Nguyễn Duy Hưng**, an information security student at the University of Information Technology, VNU-HCM.

I love building autonomous systems powered by agents and multi-agent LLMs to serve cyber security. My goal is to work in agentic security, making AI agents genuinely useful for finding and fixing real security problems.

---

## Personal project

| Project | Stack | What it does |
| --- | --- | --- |
| [**Militech**](https://github.com/Hugnd-UIT/Militech) | Python | Multi-agent system that hunts and exploits vulnerabilities across entire repositories |
| [**Arasaka**](https://github.com/Hugnd-UIT/Arasaka) | Python | Autonomous multi-agent fuzzing framework for C/C++ repositories |
| [**Kang-Tao**](https://github.com/Hugnd-UIT/Kang-Tao) | Python | Automated CTF challenge solver powered by LLMs |
| [**Budget-Arms**](https://github.com/Hugnd-UIT/Budget-Arms) | Python | Hybrid ML and LLM agent framework for DDoS defense |
| [**Trauma-Team**](https://github.com/Hugnd-UIT/Trauma-Team) | Python | LLM-driven Windows disk recovery for NTFS and FAT12/16/32 |

---

## Academic project

---

## Vulnerability research

Independently discovered and verified, each with a working proof of vulnerability confirmed under ASan.

| Library | Version | Findings | Highlights |
| --- | --- | --- | --- |
| **cJSON** | v1.7.16 | 6 zero-days | `overwrite_item` ignores `cJSON_IsReference` on root replace, leading to heap use-after-free and double-free (**CVSS 9.8 Critical**). `sort_list` breaks the `head->prev` tail invariant, causing silent data loss and a heap UAF write (**CVSS 8.2 High**). Also NULL dereferences in `cJSONUtils_strdup` and `pointer_encoded_length` (**CVSS 7.5 High**), plus infinite loop or double-free in `add_item_to_array` and a cross-tree aliasing UAF in `cJSON_ReplaceItemViaPointer`. |
| **libxls** | v1.6.4 (`34c7cc6`) | 3 bugs in BIFF8 parsing | Heap buffer overflow write of 255 bytes in `xls_getCSS` via unchecked `strcat` (**CVSS 8.8 High**, CWE-122). Global out-of-bounds read in `xls_getColor` (**5.3 Medium**). Heap buffer overflow read in `xls_parseWorkSheet` (**3.1 Low**). All reproducible with a C PoC and a crafted `.xls`. |
| **libucl** | <= 0.10.0 (`c3580720`) | 3 heap use-after-free | `ucl_hash_destroy` reads freed memory after `ucl_object_merge(copy=false)` because two `ucl_hash_t` tables share an intrusive linked-list pointer (**CVSS 7.5 High**, CWE-416). Affects projects that embed libucl, such as FreeBSD pkg and Rspamd. |

---

## Contact

- GitHub: [@Hugnd-UIT](https://github.com/Hugnd-UIT)
- Email: [hungnd.attt2024@gmail.com](mailto:hungnd.attt2024@gmail.com)

<div align="center">

`> whoami` &nbsp;->&nbsp; **Agentic security dev**

</div>
