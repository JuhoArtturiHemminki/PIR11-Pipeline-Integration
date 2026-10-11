# PIR11 MEMORY ENGINE: PROPRIETARY LICENSE AND INTELLECTUAL PROPERTY DECLARATION

**Copyright (c) 2026 Juho Artturi Hemminki. All Rights Reserved.**
**Licensing Inquiries and Commercial Requests:** projectflagcarrier@gmail.com

---

## 1. PREAMBLE AND INTELLECTUAL PROPERTY CLAIM

This document defines the strict proprietary licensing terms and architectural ownership declarations for the **PIR11 Memory Engine**, including its source code, binary representations, mathematical representations, and foundational integration methodologies.

The Owner (Juho Artturi Hemminki) asserts exclusive global Intellectual Property (IP) and technical method claims over the specific computational pipeline, kernel designs, and runtime acceleration methodologies described herein. This claim encompasses all byte-level and bit-level page-filtering logic designed to interface directly with low-level execution layers.

### Scope of Method and Architectural Claims

The scope of this protective declaration covers, but is not limited to, the following technical inventions and execution paradigms:

* **The PIR11 Vector Kernel (Bit-Density Optimization):** The specific hardware-aligned loops utilizing unrolled population counts (`__builtin_popcountll`, `vpopcntq`, or SIMD equivalents) to evaluate uniform 4096-byte hardware pages (`PAGE_SIZE_BYTES`) into deterministic entropy state outputs (`is_collapsed`).
* **Virtual Memory Page Interception (MMU/VMM Binding):** The method of translating software-calculated bitwise density metrics directly into hardware-level page protection states (such as assigning a `PROT_NONE` attribute via operating system kernels to flag a collapsed or dormant page state).
* **Hardware Exception Redirection (Zero-Overhead Control Flow):** The use of operating system signal handlers (such as catching `SIGSEGV` or Page Fault interrupts at the hardware Memory Management Unit layer) to dynamically bypass upper-level software application logic without runtime polling or conditional branches.
* **Asynchronous Streaming Double-Buffering:** The multithreaded, decoupled pipeline pattern where raw ingestion memory blocks are evaluated by background worker threads using the PIR11 core kernel concurrently with separate master execution/compute tracks.

---

## 2. LICENSE TERMS AND CONDITIONS

### 2.1. Non-Commercial and Evaluation License
Subject to the terms of this License, the Owner grants to individuals and academic institutions a limited, non-exclusive, non-transferable, royalty-free, revocable license to review, download, compile, and execute the PIR11 Memory Engine source code solely for internal, non-commercial evaluation, educational benchmarking, and research purposes.

### 2.2. Commercial Use Prohibition
Commercial exploitation, utilization, deployment, or integration of the PIR11 Memory Engine (or its underlying architecture, claimed methods, and integration concepts) within any revenue-generating software, proprietary game engines, enterprise database applications, cloud services, or hardware devices is **STRICTLY PROHIBITED** without an explicit, signed commercial license agreement from the Owner.

For all commercial licensing models, rate structures, and integration clearance, contact the Owner directly at: **projectflagcarrier@gmail.com**.

### 2.3. Restrictions
Licensees and viewers of this source code and architecture shall not:
1. Sublicense, lease, rent, redistribute, or sell the PIR11 code components or its architectural derivatives without prior written consent from the Owner.
2. Modify or incorporate the architectural page fault interception patterns (`PROT_NONE` bypass loops) into public open-source software libraries under permissive licenses (e.g., MIT, Apache 2.0, GPL) that would compromise the Owner's proprietary intellectual claims.
3. Remove, obscure, or alter any copyright notices, authorship credits (Juho Artturi Hemminki), or contact information embedded within the project files.

---

## 3. DISCLAIMER OF WARRANTY AND LIMITATION OF LIABILITY

### 3.1. No Warranty
THE PIR11 MEMORY ENGINE AND ALL ASSOCIATED DOCUMENTATION ARE PROVIDED BY THE COPYRIGHT HOLDER "AS IS". ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NON-INFRINGEMENT ARE EXPRESSLY DISCLAIMED.

### 3.2. Limitation of Liability
IN NO EVENT SHALL THE COPYRIGHT OWNER OR ITS CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE OR ITS ARCHITECTURAL METHODS, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
