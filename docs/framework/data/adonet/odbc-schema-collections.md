---
title: ODBC şeması koleksiyonları
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: 36d0859b897bfcea33803c219ade14722ed90421
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32766653"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="bbc8d-102">ODBC şeması koleksiyonları</span><span class="sxs-lookup"><span data-stu-id="bbc8d-102">ODBC Schema Collections</span></span>
<span data-ttu-id="bbc8d-103">Bu bölümde, Microsoft SQL Server, Oracle ve Microsoft Jet ODBC sürücüleri için şema koleksiyonu desteği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bbc8d-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="bbc8d-104">Microsoft SQL Server ODBC sürücüsü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="bbc8d-105">Microsoft SQL Server ODBC sürücüsü ortak şeması koleksiyonları ek olarak aşağıdaki belirli şeması koleksiyonları destekler:</span><span class="sxs-lookup"><span data-stu-id="bbc8d-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="bbc8d-106">tabloları</span><span class="sxs-lookup"><span data-stu-id="bbc8d-106">Tables</span></span>  
  
-   <span data-ttu-id="bbc8d-107">Dizinler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-107">Indexes</span></span>  
  
-   <span data-ttu-id="bbc8d-108">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-108">Columns</span></span>  
  
-   <span data-ttu-id="bbc8d-109">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-109">Procedures</span></span>  
  
-   <span data-ttu-id="bbc8d-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="bbc8d-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="bbc8d-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="bbc8d-112">Görünümler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="bbc8d-113">Tabloları ve görünümleri</span><span class="sxs-lookup"><span data-stu-id="bbc8d-113">Tables and Views</span></span>  
  
|<span data-ttu-id="bbc8d-114">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-114">ColumnName</span></span>|<span data-ttu-id="bbc8d-115">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-116">TABLE_CAT</span></span>|<span data-ttu-id="bbc8d-117">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-117">String</span></span>|  
|<span data-ttu-id="bbc8d-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-118">TABLE_SCHEM</span></span>|<span data-ttu-id="bbc8d-119">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-119">String</span></span>|  
|<span data-ttu-id="bbc8d-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-120">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-121">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-121">String</span></span>|  
|<span data-ttu-id="bbc8d-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-122">TABLE_TYPE</span></span>|<span data-ttu-id="bbc8d-123">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-123">String</span></span>|  
|<span data-ttu-id="bbc8d-124">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-124">REMARKS</span></span>|<span data-ttu-id="bbc8d-125">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="bbc8d-126">Dizinler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-126">Indexes</span></span>  
  
|<span data-ttu-id="bbc8d-127">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-127">ColumnName</span></span>|<span data-ttu-id="bbc8d-128">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-129">TABLE_CAT</span></span>|<span data-ttu-id="bbc8d-130">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-130">String</span></span>|  
|<span data-ttu-id="bbc8d-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-131">TABLE_SCHEM</span></span>|<span data-ttu-id="bbc8d-132">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-132">String</span></span>|  
|<span data-ttu-id="bbc8d-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-133">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-134">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-134">String</span></span>|  
|<span data-ttu-id="bbc8d-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-135">NON_UNIQUE</span></span>|<span data-ttu-id="bbc8d-136">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-136">Int16</span></span>|  
|<span data-ttu-id="bbc8d-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-138">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-138">String</span></span>|  
|<span data-ttu-id="bbc8d-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-139">INDEX_NAME</span></span>|<span data-ttu-id="bbc8d-140">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-140">String</span></span>|  
|<span data-ttu-id="bbc8d-141">TÜRÜ</span><span class="sxs-lookup"><span data-stu-id="bbc8d-141">TYPE</span></span>|<span data-ttu-id="bbc8d-142">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-142">Int16</span></span>|  
|<span data-ttu-id="bbc8d-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-144">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-144">Int16</span></span>|  
|<span data-ttu-id="bbc8d-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-145">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-146">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-146">String</span></span>|  
|<span data-ttu-id="bbc8d-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="bbc8d-147">ASC_OR_DESC</span></span>|<span data-ttu-id="bbc8d-148">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-148">String</span></span>|  
|<span data-ttu-id="bbc8d-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="bbc8d-149">CARDINATLITY</span></span>|<span data-ttu-id="bbc8d-150">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-150">Int32</span></span>|  
|<span data-ttu-id="bbc8d-151">SAYFALARI</span><span class="sxs-lookup"><span data-stu-id="bbc8d-151">PAGES</span></span>|<span data-ttu-id="bbc8d-152">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-152">Int32</span></span>|  
|<span data-ttu-id="bbc8d-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-153">FILTER_CONDITION</span></span>|<span data-ttu-id="bbc8d-154">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-154">String</span></span>|  
|<span data-ttu-id="bbc8d-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="bbc8d-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="bbc8d-156">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-156">String</span></span>|  
|<span data-ttu-id="bbc8d-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-158">Bayt</span><span class="sxs-lookup"><span data-stu-id="bbc8d-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="bbc8d-159">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-159">Columns</span></span>  
  
|<span data-ttu-id="bbc8d-160">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-160">ColumnName</span></span>|<span data-ttu-id="bbc8d-161">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-162">TABLE_CAT</span></span>|<span data-ttu-id="bbc8d-163">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-163">String</span></span>|  
|<span data-ttu-id="bbc8d-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-164">TABLE_SCHEM</span></span>|<span data-ttu-id="bbc8d-165">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-165">String</span></span>|  
|<span data-ttu-id="bbc8d-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-166">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-167">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-167">String</span></span>|  
|<span data-ttu-id="bbc8d-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-168">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-169">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-169">String</span></span>|  
|<span data-ttu-id="bbc8d-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-170">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-171">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-171">Int16</span></span>|  
|<span data-ttu-id="bbc8d-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-172">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-173">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-173">String</span></span>|  
|<span data-ttu-id="bbc8d-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-174">COLUMN_SIZE</span></span>|<span data-ttu-id="bbc8d-175">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-175">Int32</span></span>|  
|<span data-ttu-id="bbc8d-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="bbc8d-177">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-177">Int32</span></span>|  
|<span data-ttu-id="bbc8d-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="bbc8d-179">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-179">Int16</span></span>|  
|<span data-ttu-id="bbc8d-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="bbc8d-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="bbc8d-181">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-181">Int16</span></span>|  
|<span data-ttu-id="bbc8d-182">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-182">NULLABLE</span></span>|<span data-ttu-id="bbc8d-183">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-183">Int16</span></span>|  
|<span data-ttu-id="bbc8d-184">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-184">REMARKS</span></span>|<span data-ttu-id="bbc8d-185">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-185">String</span></span>|  
|<span data-ttu-id="bbc8d-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="bbc8d-186">COLUMN_DEF</span></span>|<span data-ttu-id="bbc8d-187">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-187">String</span></span>|  
|<span data-ttu-id="bbc8d-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-189">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-189">Int16</span></span>|  
|<span data-ttu-id="bbc8d-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="bbc8d-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="bbc8d-191">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-191">Int16</span></span>|  
|<span data-ttu-id="bbc8d-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="bbc8d-193">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-193">Int32</span></span>|  
|<span data-ttu-id="bbc8d-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-195">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-195">Int32</span></span>|  
|<span data-ttu-id="bbc8d-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-196">IS_NULLABLE</span></span>|<span data-ttu-id="bbc8d-197">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-197">String</span></span>|  
|<span data-ttu-id="bbc8d-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="bbc8d-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="bbc8d-199">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-199">String</span></span>|  
|<span data-ttu-id="bbc8d-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="bbc8d-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="bbc8d-201">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-201">String</span></span>|  
|<span data-ttu-id="bbc8d-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-203">Bayt</span><span class="sxs-lookup"><span data-stu-id="bbc8d-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="bbc8d-204">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-204">Procedures</span></span>  
  
|<span data-ttu-id="bbc8d-205">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-205">ColumnName</span></span>|<span data-ttu-id="bbc8d-206">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="bbc8d-208">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-208">String</span></span>|  
|<span data-ttu-id="bbc8d-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="bbc8d-210">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-210">String</span></span>|  
|<span data-ttu-id="bbc8d-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-212">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-212">String</span></span>|  
|<span data-ttu-id="bbc8d-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-214">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-214">Int32</span></span>|  
|<span data-ttu-id="bbc8d-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-216">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-216">Int32</span></span>|  
|<span data-ttu-id="bbc8d-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="bbc8d-218">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-218">Int32</span></span>|  
|<span data-ttu-id="bbc8d-219">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-219">REMARKS</span></span>|<span data-ttu-id="bbc8d-220">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-220">String</span></span>|  
|<span data-ttu-id="bbc8d-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="bbc8d-222">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="bbc8d-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="bbc8d-224">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-224">ColumnName</span></span>|<span data-ttu-id="bbc8d-225">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="bbc8d-227">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-227">String</span></span>|  
|<span data-ttu-id="bbc8d-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="bbc8d-229">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-229">String</span></span>|  
|<span data-ttu-id="bbc8d-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-231">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-231">String</span></span>|  
|<span data-ttu-id="bbc8d-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-232">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-233">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-233">String</span></span>|  
|<span data-ttu-id="bbc8d-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-234">COLUMN_TYPE</span></span>|<span data-ttu-id="bbc8d-235">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-235">Int16</span></span>|  
|<span data-ttu-id="bbc8d-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-236">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-237">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-237">Int16</span></span>|  
|<span data-ttu-id="bbc8d-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-238">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-239">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-239">String</span></span>|  
|<span data-ttu-id="bbc8d-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-240">COLUMN_SIZE</span></span>|<span data-ttu-id="bbc8d-241">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-241">Int32</span></span>|  
|<span data-ttu-id="bbc8d-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="bbc8d-243">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-243">Int32</span></span>|  
|<span data-ttu-id="bbc8d-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="bbc8d-245">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-245">Int16</span></span>|  
|<span data-ttu-id="bbc8d-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="bbc8d-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="bbc8d-247">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-247">Int16</span></span>|  
|<span data-ttu-id="bbc8d-248">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-248">NULLABLE</span></span>|<span data-ttu-id="bbc8d-249">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-249">Int16</span></span>|  
|<span data-ttu-id="bbc8d-250">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-250">REMARKS</span></span>|<span data-ttu-id="bbc8d-251">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-251">String</span></span>|  
|<span data-ttu-id="bbc8d-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="bbc8d-252">COLUMN_DEF</span></span>|<span data-ttu-id="bbc8d-253">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-253">String</span></span>|  
|<span data-ttu-id="bbc8d-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-255">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-255">Int16</span></span>|  
|<span data-ttu-id="bbc8d-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="bbc8d-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="bbc8d-257">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-257">Int16</span></span>|  
|<span data-ttu-id="bbc8d-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="bbc8d-259">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-259">Int32</span></span>|  
|<span data-ttu-id="bbc8d-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-261">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-261">Int32</span></span>|  
|<span data-ttu-id="bbc8d-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-262">IS_NULLABLE</span></span>|<span data-ttu-id="bbc8d-263">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-263">String</span></span>|  
|<span data-ttu-id="bbc8d-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="bbc8d-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="bbc8d-265">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-265">String</span></span>|  
|<span data-ttu-id="bbc8d-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="bbc8d-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="bbc8d-267">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-267">String</span></span>|  
|<span data-ttu-id="bbc8d-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-269">Bayt</span><span class="sxs-lookup"><span data-stu-id="bbc8d-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="bbc8d-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="bbc8d-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="bbc8d-271">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-271">ColumnName</span></span>|<span data-ttu-id="bbc8d-272">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="bbc8d-274">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-274">String</span></span>|  
|<span data-ttu-id="bbc8d-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="bbc8d-276">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-276">String</span></span>|  
|<span data-ttu-id="bbc8d-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-278">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-278">String</span></span>|  
|<span data-ttu-id="bbc8d-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-279">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-280">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-280">String</span></span>|  
|<span data-ttu-id="bbc8d-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-281">COLUMN_TYPE</span></span>|<span data-ttu-id="bbc8d-282">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-282">Int16</span></span>|  
|<span data-ttu-id="bbc8d-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-283">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-284">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-284">Int16</span></span>|  
|<span data-ttu-id="bbc8d-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-285">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-286">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-286">String</span></span>|  
|<span data-ttu-id="bbc8d-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-287">COLUMN_SIZE</span></span>|<span data-ttu-id="bbc8d-288">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-288">Int32</span></span>|  
|<span data-ttu-id="bbc8d-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="bbc8d-290">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-290">Int32</span></span>|  
|<span data-ttu-id="bbc8d-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="bbc8d-292">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-292">Int16</span></span>|  
|<span data-ttu-id="bbc8d-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="bbc8d-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="bbc8d-294">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-294">Int16</span></span>|  
|<span data-ttu-id="bbc8d-295">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-295">NULLABLE</span></span>|<span data-ttu-id="bbc8d-296">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-296">Int16</span></span>|  
|<span data-ttu-id="bbc8d-297">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-297">REMARKS</span></span>|<span data-ttu-id="bbc8d-298">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-298">String</span></span>|  
|<span data-ttu-id="bbc8d-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="bbc8d-299">COLUMN_DEF</span></span>|<span data-ttu-id="bbc8d-300">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-300">String</span></span>|  
|<span data-ttu-id="bbc8d-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-302">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-302">Int16</span></span>|  
|<span data-ttu-id="bbc8d-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="bbc8d-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="bbc8d-304">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-304">Int16</span></span>|  
|<span data-ttu-id="bbc8d-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="bbc8d-306">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-306">Int32</span></span>|  
|<span data-ttu-id="bbc8d-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-308">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-308">Int32</span></span>|  
|<span data-ttu-id="bbc8d-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-309">IS_NULLABLE</span></span>|<span data-ttu-id="bbc8d-310">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-310">String</span></span>|  
|<span data-ttu-id="bbc8d-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="bbc8d-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="bbc8d-312">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-312">String</span></span>|  
|<span data-ttu-id="bbc8d-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="bbc8d-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="bbc8d-314">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-314">String</span></span>|  
|<span data-ttu-id="bbc8d-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-316">Bayt</span><span class="sxs-lookup"><span data-stu-id="bbc8d-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="bbc8d-317">Microsoft Oracle ODBC sürücüsü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="bbc8d-318">Microsoft SQL Server Oracle ODBC sürücüsü ortak şeması koleksiyonları ek olarak aşağıdaki belirli şeması koleksiyonları destekler:</span><span class="sxs-lookup"><span data-stu-id="bbc8d-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="bbc8d-319">tabloları</span><span class="sxs-lookup"><span data-stu-id="bbc8d-319">Tables</span></span>  
  
-   <span data-ttu-id="bbc8d-320">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-320">Columns</span></span>  
  
-   <span data-ttu-id="bbc8d-321">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-321">Procedures</span></span>  
  
-   <span data-ttu-id="bbc8d-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="bbc8d-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="bbc8d-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="bbc8d-324">Görünümler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-324">Views</span></span>  
  
-   <span data-ttu-id="bbc8d-325">Dizinler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="bbc8d-326">Tabloları ve görünümleri</span><span class="sxs-lookup"><span data-stu-id="bbc8d-326">Tables and Views</span></span>  
  
|<span data-ttu-id="bbc8d-327">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-327">ColumnName</span></span>|<span data-ttu-id="bbc8d-328">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-330">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-330">String</span></span>|  
|<span data-ttu-id="bbc8d-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-331">TABLE_OWNER</span></span>|<span data-ttu-id="bbc8d-332">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-332">String</span></span>|  
|<span data-ttu-id="bbc8d-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-333">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-334">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-334">String</span></span>|  
|<span data-ttu-id="bbc8d-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-335">TABLE_TYPE</span></span>|<span data-ttu-id="bbc8d-336">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-336">String</span></span>|  
|<span data-ttu-id="bbc8d-337">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-337">REMARKS</span></span>|<span data-ttu-id="bbc8d-338">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="bbc8d-339">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-339">Columns</span></span>  
  
|<span data-ttu-id="bbc8d-340">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-340">ColumnName</span></span>|<span data-ttu-id="bbc8d-341">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-343">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-343">String</span></span>|  
|<span data-ttu-id="bbc8d-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-344">TABLE_OWNER</span></span>|<span data-ttu-id="bbc8d-345">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-345">String</span></span>|  
|<span data-ttu-id="bbc8d-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-346">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-347">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-347">String</span></span>|  
|<span data-ttu-id="bbc8d-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-348">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-349">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-349">String</span></span>|  
|<span data-ttu-id="bbc8d-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-350">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-351">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-351">Int16</span></span>|  
|<span data-ttu-id="bbc8d-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-352">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-353">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-353">String</span></span>|  
|<span data-ttu-id="bbc8d-354">DUYARLILIK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-354">PRECISION</span></span>|<span data-ttu-id="bbc8d-355">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-355">Int32</span></span>|  
|<span data-ttu-id="bbc8d-356">UZUNLUĞU</span><span class="sxs-lookup"><span data-stu-id="bbc8d-356">LENGTH</span></span>|<span data-ttu-id="bbc8d-357">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-357">Int32</span></span>|  
|<span data-ttu-id="bbc8d-358">ÖLÇEK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-358">SCALE</span></span>|<span data-ttu-id="bbc8d-359">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-359">Int16</span></span>|  
|<span data-ttu-id="bbc8d-360">SAYI TABANINI</span><span class="sxs-lookup"><span data-stu-id="bbc8d-360">RADIX</span></span>|<span data-ttu-id="bbc8d-361">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-361">Int16</span></span>|  
|<span data-ttu-id="bbc8d-362">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-362">NULLABLE</span></span>|<span data-ttu-id="bbc8d-363">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-363">Int16</span></span>|  
|<span data-ttu-id="bbc8d-364">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-364">REMARKS</span></span>|<span data-ttu-id="bbc8d-365">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-365">String</span></span>|  
|<span data-ttu-id="bbc8d-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-367">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="bbc8d-368">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-368">Procedures</span></span>  
  
|<span data-ttu-id="bbc8d-369">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-369">ColumnName</span></span>|<span data-ttu-id="bbc8d-370">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-372">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-372">String</span></span>|  
|<span data-ttu-id="bbc8d-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="bbc8d-374">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-374">String</span></span>|  
|<span data-ttu-id="bbc8d-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-376">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-376">String</span></span>|  
|<span data-ttu-id="bbc8d-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-378">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-378">Int16</span></span>|  
|<span data-ttu-id="bbc8d-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-380">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-380">Int16</span></span>|  
|<span data-ttu-id="bbc8d-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="bbc8d-382">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-382">Int16</span></span>|  
|<span data-ttu-id="bbc8d-383">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-383">REMARKS</span></span>|<span data-ttu-id="bbc8d-384">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-384">String</span></span>|  
|<span data-ttu-id="bbc8d-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="bbc8d-386">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="bbc8d-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="bbc8d-388">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-388">ColumnName</span></span>|<span data-ttu-id="bbc8d-389">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-391">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-391">String</span></span>|  
|<span data-ttu-id="bbc8d-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="bbc8d-393">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-393">String</span></span>|  
|<span data-ttu-id="bbc8d-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-395">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-395">String</span></span>|  
|<span data-ttu-id="bbc8d-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-396">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-397">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-397">String</span></span>|  
|<span data-ttu-id="bbc8d-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-398">COLUMN_TYPE</span></span>|<span data-ttu-id="bbc8d-399">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-399">Int16</span></span>|  
|<span data-ttu-id="bbc8d-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-400">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-401">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-401">Int16</span></span>|  
|<span data-ttu-id="bbc8d-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-402">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-403">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-403">String</span></span>|  
|<span data-ttu-id="bbc8d-404">DUYARLILIK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-404">PRECISION</span></span>|<span data-ttu-id="bbc8d-405">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-405">Int32</span></span>|  
|<span data-ttu-id="bbc8d-406">UZUNLUĞU</span><span class="sxs-lookup"><span data-stu-id="bbc8d-406">LENGTH</span></span>|<span data-ttu-id="bbc8d-407">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-407">Int32</span></span>|  
|<span data-ttu-id="bbc8d-408">ÖLÇEK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-408">SCALE</span></span>|<span data-ttu-id="bbc8d-409">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-409">Int16</span></span>|  
|<span data-ttu-id="bbc8d-410">SAYI TABANINI</span><span class="sxs-lookup"><span data-stu-id="bbc8d-410">RADIX</span></span>|<span data-ttu-id="bbc8d-411">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-411">Int16</span></span>|  
|<span data-ttu-id="bbc8d-412">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-412">NULLABLE</span></span>|<span data-ttu-id="bbc8d-413">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-413">Int16</span></span>|  
|<span data-ttu-id="bbc8d-414">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-414">REMARKS</span></span>|<span data-ttu-id="bbc8d-415">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-415">String</span></span>|  
|<span data-ttu-id="bbc8d-416">AŞIRI YÜKLEME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-416">OVERLOAD</span></span>|<span data-ttu-id="bbc8d-417">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-417">Int32</span></span>|  
|<span data-ttu-id="bbc8d-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-419">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="bbc8d-420">Microsoft Jet ODBC sürücüsü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="bbc8d-421">Microsoft Jet ODBC sürücüsü ortak şeması koleksiyonları ek olarak aşağıdaki belirli şeması koleksiyonları destekler:</span><span class="sxs-lookup"><span data-stu-id="bbc8d-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="bbc8d-422">tabloları</span><span class="sxs-lookup"><span data-stu-id="bbc8d-422">Tables</span></span>  
  
-   <span data-ttu-id="bbc8d-423">Dizinler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-423">Indexes</span></span>  
  
-   <span data-ttu-id="bbc8d-424">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-424">Columns</span></span>  
  
-   <span data-ttu-id="bbc8d-425">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-425">Procedures</span></span>  
  
-   <span data-ttu-id="bbc8d-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="bbc8d-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="bbc8d-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="bbc8d-428">Görünümler</span><span class="sxs-lookup"><span data-stu-id="bbc8d-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="bbc8d-429">Tabloları ve görünümleri</span><span class="sxs-lookup"><span data-stu-id="bbc8d-429">Tables and Views</span></span>  
  
|<span data-ttu-id="bbc8d-430">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-430">ColumnName</span></span>|<span data-ttu-id="bbc8d-431">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-433">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-433">String</span></span>|  
|<span data-ttu-id="bbc8d-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-434">TABLE_OWNER</span></span>|<span data-ttu-id="bbc8d-435">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-435">String</span></span>|  
|<span data-ttu-id="bbc8d-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-436">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-437">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-437">String</span></span>|  
|<span data-ttu-id="bbc8d-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-438">TABLE_TYPE</span></span>|<span data-ttu-id="bbc8d-439">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-439">String</span></span>|  
|<span data-ttu-id="bbc8d-440">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-440">REMARKS</span></span>|<span data-ttu-id="bbc8d-441">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="bbc8d-442">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-442">Columns</span></span>  
  
|<span data-ttu-id="bbc8d-443">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-443">ColumnName</span></span>|<span data-ttu-id="bbc8d-444">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-446">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-446">String</span></span>|  
|<span data-ttu-id="bbc8d-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-447">TABLE_OWNER</span></span>|<span data-ttu-id="bbc8d-448">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-448">String</span></span>|  
|<span data-ttu-id="bbc8d-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-449">TABLE_NAME</span></span>|<span data-ttu-id="bbc8d-450">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-450">String</span></span>|  
|<span data-ttu-id="bbc8d-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-451">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-452">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-452">String</span></span>|  
|<span data-ttu-id="bbc8d-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-453">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-454">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-454">Int16</span></span>|  
|<span data-ttu-id="bbc8d-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-455">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-456">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-456">String</span></span>|  
|<span data-ttu-id="bbc8d-457">DUYARLILIK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-457">PRECISION</span></span>|<span data-ttu-id="bbc8d-458">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-458">Int32</span></span>|  
|<span data-ttu-id="bbc8d-459">UZUNLUĞU</span><span class="sxs-lookup"><span data-stu-id="bbc8d-459">LENGTH</span></span>|<span data-ttu-id="bbc8d-460">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-460">Int32</span></span>|  
|<span data-ttu-id="bbc8d-461">ÖLÇEK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-461">SCALE</span></span>|<span data-ttu-id="bbc8d-462">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-462">Int16</span></span>|  
|<span data-ttu-id="bbc8d-463">SAYI TABANINI</span><span class="sxs-lookup"><span data-stu-id="bbc8d-463">RADIX</span></span>|<span data-ttu-id="bbc8d-464">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-464">Int16</span></span>|  
|<span data-ttu-id="bbc8d-465">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-465">NULLABLE</span></span>|<span data-ttu-id="bbc8d-466">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-466">Int16</span></span>|  
|<span data-ttu-id="bbc8d-467">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-467">REMARKS</span></span>|<span data-ttu-id="bbc8d-468">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-468">String</span></span>|  
|<span data-ttu-id="bbc8d-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-470">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="bbc8d-471">Yordamlar</span><span class="sxs-lookup"><span data-stu-id="bbc8d-471">Procedures</span></span>  
  
|<span data-ttu-id="bbc8d-472">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-472">ColumnName</span></span>|<span data-ttu-id="bbc8d-473">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-475">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-475">String</span></span>|  
|<span data-ttu-id="bbc8d-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="bbc8d-477">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-477">String</span></span>|  
|<span data-ttu-id="bbc8d-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-479">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-479">String</span></span>|  
|<span data-ttu-id="bbc8d-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-481">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-481">Int16</span></span>|  
|<span data-ttu-id="bbc8d-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="bbc8d-483">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-483">Int16</span></span>|  
|<span data-ttu-id="bbc8d-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="bbc8d-485">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-485">Int16</span></span>|  
|<span data-ttu-id="bbc8d-486">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-486">REMARKS</span></span>|<span data-ttu-id="bbc8d-487">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-487">String</span></span>|  
|<span data-ttu-id="bbc8d-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="bbc8d-489">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="bbc8d-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="bbc8d-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="bbc8d-491">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-491">ColumnName</span></span>|<span data-ttu-id="bbc8d-492">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="bbc8d-494">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-494">String</span></span>|  
|<span data-ttu-id="bbc8d-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbc8d-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="bbc8d-496">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-496">String</span></span>|  
|<span data-ttu-id="bbc8d-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-498">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-498">String</span></span>|  
|<span data-ttu-id="bbc8d-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-499">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-500">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-500">String</span></span>|  
|<span data-ttu-id="bbc8d-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-501">COLUMN_TYPE</span></span>|<span data-ttu-id="bbc8d-502">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-502">Int16</span></span>|  
|<span data-ttu-id="bbc8d-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-503">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-504">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-504">Int16</span></span>|  
|<span data-ttu-id="bbc8d-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-505">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-506">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-506">String</span></span>|  
|<span data-ttu-id="bbc8d-507">DUYARLILIK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-507">PRECISION</span></span>|<span data-ttu-id="bbc8d-508">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-508">Int32</span></span>|  
|<span data-ttu-id="bbc8d-509">UZUNLUĞU</span><span class="sxs-lookup"><span data-stu-id="bbc8d-509">LENGTH</span></span>|<span data-ttu-id="bbc8d-510">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-510">Int32</span></span>|  
|<span data-ttu-id="bbc8d-511">ÖLÇEK</span><span class="sxs-lookup"><span data-stu-id="bbc8d-511">SCALE</span></span>|<span data-ttu-id="bbc8d-512">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-512">Int16</span></span>|  
|<span data-ttu-id="bbc8d-513">SAYI TABANINI</span><span class="sxs-lookup"><span data-stu-id="bbc8d-513">RADIX</span></span>|<span data-ttu-id="bbc8d-514">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-514">Int16</span></span>|  
|<span data-ttu-id="bbc8d-515">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-515">NULLABLE</span></span>|<span data-ttu-id="bbc8d-516">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-516">Int16</span></span>|  
|<span data-ttu-id="bbc8d-517">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-517">REMARKS</span></span>|<span data-ttu-id="bbc8d-518">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-518">String</span></span>|  
|<span data-ttu-id="bbc8d-519">AŞIRI YÜKLEME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-519">OVERLOAD</span></span>|<span data-ttu-id="bbc8d-520">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-520">Int32</span></span>|  
|<span data-ttu-id="bbc8d-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-522">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="bbc8d-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="bbc8d-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="bbc8d-524">columnName</span><span class="sxs-lookup"><span data-stu-id="bbc8d-524">ColumnName</span></span>|<span data-ttu-id="bbc8d-525">Veri türü</span><span class="sxs-lookup"><span data-stu-id="bbc8d-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="bbc8d-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="bbc8d-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="bbc8d-527">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-527">String</span></span>|  
|<span data-ttu-id="bbc8d-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="bbc8d-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="bbc8d-529">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-529">String</span></span>|  
|<span data-ttu-id="bbc8d-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="bbc8d-531">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-531">String</span></span>|  
|<span data-ttu-id="bbc8d-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-532">COLUMN_NAME</span></span>|<span data-ttu-id="bbc8d-533">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-533">String</span></span>|  
|<span data-ttu-id="bbc8d-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-534">COLUMN_TYPE</span></span>|<span data-ttu-id="bbc8d-535">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-535">Int16</span></span>|  
|<span data-ttu-id="bbc8d-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-536">DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-537">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-537">Int16</span></span>|  
|<span data-ttu-id="bbc8d-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbc8d-538">TYPE_NAME</span></span>|<span data-ttu-id="bbc8d-539">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-539">String</span></span>|  
|<span data-ttu-id="bbc8d-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-540">COLUMN_SIZE</span></span>|<span data-ttu-id="bbc8d-541">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-541">Int32</span></span>|  
|<span data-ttu-id="bbc8d-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="bbc8d-543">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-543">Int32</span></span>|  
|<span data-ttu-id="bbc8d-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="bbc8d-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="bbc8d-545">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-545">Int16</span></span>|  
|<span data-ttu-id="bbc8d-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="bbc8d-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="bbc8d-547">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-547">Int16</span></span>|  
|<span data-ttu-id="bbc8d-548">BOŞ DEĞER ATANABİLİR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-548">NULLABLE</span></span>|<span data-ttu-id="bbc8d-549">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-549">Int16</span></span>|  
|<span data-ttu-id="bbc8d-550">AÇIKLAMALAR</span><span class="sxs-lookup"><span data-stu-id="bbc8d-550">REMARKS</span></span>|<span data-ttu-id="bbc8d-551">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-551">String</span></span>|  
|<span data-ttu-id="bbc8d-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="bbc8d-552">COLUMN_DEF</span></span>|<span data-ttu-id="bbc8d-553">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-553">String</span></span>|  
|<span data-ttu-id="bbc8d-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="bbc8d-555">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-555">Int16</span></span>|  
|<span data-ttu-id="bbc8d-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="bbc8d-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="bbc8d-557">Int16</span><span class="sxs-lookup"><span data-stu-id="bbc8d-557">Int16</span></span>|  
|<span data-ttu-id="bbc8d-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="bbc8d-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="bbc8d-559">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-559">Int32</span></span>|  
|<span data-ttu-id="bbc8d-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="bbc8d-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="bbc8d-561">Int32</span><span class="sxs-lookup"><span data-stu-id="bbc8d-561">Int32</span></span>|  
|<span data-ttu-id="bbc8d-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="bbc8d-562">IS_NULLABLE</span></span>|<span data-ttu-id="bbc8d-563">Dize</span><span class="sxs-lookup"><span data-stu-id="bbc8d-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bbc8d-564">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="bbc8d-564">See Also</span></span>  
 [<span data-ttu-id="bbc8d-565">ADO.NET yönetilen sağlayıcıları ve veri kümesi Geliştirici Merkezi</span><span class="sxs-lookup"><span data-stu-id="bbc8d-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
