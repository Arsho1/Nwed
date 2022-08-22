(function(BLAZE) {
    BLAZE.PhHkha = function() {
        document.title = 'Gamezer';
        if (!dLeLMm.HahjNP()) {
            var ldIhkf = document.createElement('div');
            ldIhkf.className = 'icon_unsupported_html5';
            document.body.appendChild(ldIhkf);
            return false;
        };
        BLAZE.bKgEdk.bfjEAd('system', 'exit', PlONBA);
        BLAZE.bKgEdk.bfjEAd('system', 'start', omaAmB);
        BLAZE.bKgEdk.bfjEAd('GameSystem', 'ploBBK', IKNKHi);
        return true;
    };

    function PlONBA() {
        if (BLAZE.fGLhHJ) { BLAZE.fGLhHJ.HjKaLb(); };
        if (BLAZE.pdpIcA) { BLAZE.pdpIcA.HjKaLb(); };
        if (BLAZE.gpMPfm) { BLAZE.gpMPfm.HjKaLb(); };
        if (arguments[2] == 'unload') { return; };
        var KnjnmC;
        var ldIhkf = document.createElement('div');
        ldIhkf.id = 'BLAZE_Exit';
        document.body.appendChild(ldIhkf);
        if (arguments[2] == 'resource') { KnjnmC = IpFeae('exit_resource').replace('{URL}', 'javascript:BLAZE.global.gs.re()'); } else if (arguments[2] == 'version') { KnjnmC = IpFeae('exit_version'); } else if (arguments[2] == 'unique') { KnjnmC = IpFeae('exit_unique'); } else { KnjnmC = IpFeae('exit_error') + '<br>' + arguments[2]; };
        ldIhkf.innerHTML = KnjnmC;
    };

    function IKNKHi() { if (BLAZE.gpMPfm) { if (BLAZE.PLATFORM == 'facebook') { BLAZE.gpMPfm.CnhLiJ('auth.standby'); } else { BLAZE.gpMPfm.CnhLiJ('auth.entrance'); } }; };

    function omaAmB() { if (BLAZE.GetENV('auth') == 1) { BLAZE.fGLhHJ.OLBcNb(); } else { IKNKHi(); } };
    var oeefop = (function() {
        var aaPJke = BLAZE.GetENV('PROJECT_CONTENT_URL');
        var ELIecl = {};
        ELIecl.billiards = {};
        ELIecl.billiards['gzpool'] = true;
        ELIecl.billiards['straight'] = true;
        ELIecl.billiards['8ball'] = true;
        ELIecl.billiards['9ball'] = true;
        ELIecl.billiards['snooker'] = true;
        ELIecl.billiards['snookerplus'] = true;
        ELIecl.billiards['pyramid'] = true;
        ELIecl.billiards['scrpyramid'] = true;
        ELIecl.billiards['carom'] = true;
        ELIecl.billiards['onepocket'] = true;
        ELIecl.billiards['anyeight'] = true;
        ELIecl.billiards['bank'] = true;
        ELIecl.billiards['combo'] = true;
        ELIecl.billiards['scoreball'] = true;
        ELIecl.chess = { gzchess: true };
        ELIecl.checkers = { gzcheckers: true, amcheckers: true, anticheckers: true };
        var aGEjAM = {};
        aGEjAM.jnnpfp = function() {
            if (KAHDeb) { return null; };
            KAHDeb = true;
            return EpDMcA;
        };
        var KAHDeb = false;
        var EpDMcA = {};
        EpDMcA.FJJloK = function(EBiAiA, lMbEaF) {
            for (var MjPgFP in EBiAiA) {
                if (ELIecl.hasOwnProperty(MjPgFP)) {
                    var HEFekh = EBiAiA[MjPgFP].split(':');
                    var cIhEIM = HEFekh.length;
                    if (cIhEIM == 5) {
                        for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { HEFekh[cJcdCM] = dCibpa(HEFekh[cJcdCM]); };
                        lMbEaF[MjPgFP] = HEFekh;
                    }
                };
            }
        };
        EpDMcA.mmeagf = function(nnBfPE, nICnHB) { var HEFekh = nnBfPE.split(':'); var cIhEIM = HEFekh.length; if (cIhEIM == 5) { for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { nICnHB[cJcdCM] += dCibpa(HEFekh[cJcdCM]); if (nICnHB[cJcdCM] < 0) { nICnHB[cJcdCM] = 0; } }; } };
        EpDMcA.bmamFL = function(EBiAiA, GigegA) {
            var HnEjij = GigegA.stats_content.GigegA;
            var IIPBoc = [0, 0, 0, 0, 0];
            var gFiOmG = false;
            for (var MjPgFP in ELIecl) {
                var PlGOED = 'game_' + MjPgFP;
                if (EBiAiA.hasOwnProperty(MjPgFP)) {
                    var ilcBeA = EBiAiA[MjPgFP].split(':');
                    if (ilcBeA.length == 5) {
                        for (var cJcdCM = 0; cJcdCM < 5; cJcdCM++) {
                            ilcBeA[cJcdCM] = dCibpa(ilcBeA[cJcdCM]);
                            IIPBoc[cJcdCM] += ilcBeA[cJcdCM];
                        };
                        if (HnEjij[PlGOED] && ilcBeA[2] > 0) {
                            HnEjij[PlGOED].style.display = '';
                            HnEjij[MjPgFP + '_score'].innerHTML = ilcBeA[0];
                            HnEjij[MjPgFP + '_played'].innerHTML = ilcBeA[2];
                            HnEjij[MjPgFP + '_won'].innerHTML = ilcBeA[3];
                            HnEjij[MjPgFP + '_refused'].innerHTML = ilcBeA[4];
                            gFiOmG = true;
                            continue;
                        }
                    };
                };
                if (HnEjij[PlGOED]) { HnEjij[PlGOED].style.display = 'none'; }
            };
            if (gFiOmG) { HnEjij.no_stats.style.display = 'none'; } else { HnEjij.no_stats.style.display = ''; };
            GigegA.score.innerHTML = IpFeae('user_overall_score').replace('[n]', '<b>' + HiMfgN.dcahnC(IIPBoc[0] * 0.01) + '</b>');
            GigegA.ggvotes.innerHTML = IpFeae('user_overall_ggvotes').replace('[n]', '<b>' + IIPBoc[1] + '</b>');
        };
        EpDMcA.NcJCFL = function(EBiAiA, GigegA) {
            var HnEjij = GigegA.stats_content.GigegA;
            var DBLDLn = false;
            var LKmfKe = 0;
            var bMhAcP = 0;
            for (var MjPgFP in ELIecl) {
                var fjEJad = HnEjij['game_' + MjPgFP];
                if (EBiAiA.hasOwnProperty(MjPgFP)) {
                    var HEFekh = EBiAiA[MjPgFP];
                    if (HEFekh[2] > 0) {
                        DBLDLn = true;
                        LKmfKe += HEFekh[0];
                        bMhAcP += HEFekh[1];
                        fjEJad.style.display = '';
                        HnEjij[MjPgFP + '_score'].innerHTML = HEFekh[0];
                        HnEjij[MjPgFP + '_played'].innerHTML = HEFekh[2];
                        HnEjij[MjPgFP + '_won'].innerHTML = HEFekh[3];
                        HnEjij[MjPgFP + '_refused'].innerHTML = HEFekh[4];
                        continue;
                    }
                };
                fjEJad.style.display = 'none';
            };
            if (!DBLDLn) { HnEjij.no_stats.style.display = ''; } else { HnEjij.no_stats.style.display = 'none'; };
            GigegA.score.innerHTML = IpFeae('user_overall_score').replace('[n]', '<b>' + HiMfgN.dcahnC(LKmfKe * 0.01) + '</b>');
            GigegA.ggvotes.innerHTML = IpFeae('user_overall_ggvotes').replace('[n]', '<b>' + bMhAcP + '</b>');
        };
        EpDMcA.ieKhaC = function(bNPkJJ) {
            if (!bNPkJJ) { return; };
            var GigegA = bNPkJJ.GigegA;
            for (var FIDbFh in ELIecl) {
                var hmhILk = GigegA[FIDbFh + '_type'];
                var pjjKEO = 'game_' + FIDbFh + '_';
                if (hmhILk) {
                    var khFnEl = ELIecl[FIDbFh];
                    for (var HiboBd in khFnEl) {
                        var MnkekN = document.createElement('option');
                        MnkekN.value = HiboBd;
                        MnkekN.innerHTML = IpFeae(pjjKEO + HiboBd);
                        hmhILk.appendChild(MnkekN);
                    }
                };
            }
        };
        EpDMcA.DeCBgn = function(IhOeEc) {
            if (!IhOeEc) { return; };
            var GigegA = IhOeEc.GigegA;
            for (var FIDbFh in ELIecl) {
                var hmhILk = GigegA[FIDbFh + '_start_type'];
                var pjjKEO = 'game_' + FIDbFh + '_';
                if (hmhILk) {
                    var khFnEl = ELIecl[FIDbFh];
                    for (var HiboBd in khFnEl) {
                        var MnkekN = document.createElement('option');
                        MnkekN.value = HiboBd;
                        MnkekN.innerHTML = IpFeae(pjjKEO + HiboBd);
                        hmhILk.appendChild(MnkekN);
                    }
                };
            }
        };
        EpDMcA.OJoGBE = function(hmhILk, IikIpK) {
            IikIpK = String(IikIpK);
            if (hmhILk.fnKPFg === IikIpK) { return; };
            hmhILk.fnKPFg = IikIpK;
            dLeLMm.MDIllm(hmhILk);
            var fgEAcn;
            if (IikIpK != '') {
                if (!ELIecl.hasOwnProperty(IikIpK)) { return; };
                fgEAcn = [IikIpK];
            } else { fgEAcn = Object.keys(ELIecl); };
            var MnkekN, AcagjM, pjjKEO, khFnEl, cIhEIM = fgEAcn.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                var FIDbFh = fgEAcn[cJcdCM];
                AcagjM = FIDbFh + ':';
                pjjKEO = 'game_' + FIDbFh + '_';
                MnkekN = document.createElement('option');
                MnkekN.className = 'game_title';
                MnkekN.value = AcagjM;
                MnkekN.innerHTML = IpFeae('game_' + FIDbFh);
                hmhILk.appendChild(MnkekN);
                khFnEl = ELIecl[FIDbFh];
                for (var HiboBd in khFnEl) {
                    MnkekN = document.createElement('option');
                    MnkekN.value = AcagjM + HiboBd;
                    MnkekN.innerHTML = IpFeae(pjjKEO + HiboBd);
                    hmhILk.appendChild(MnkekN);
                }
            };
        };
        EpDMcA.iIeBam = function(lBONbL, ajJgBK) {
            var ajJgBK = String(ajJgBK).split('$');
            var PfIHKb, iBamkN, cJcdCM, cIhEIM = ajJgBK.length;
            if (cIhEIM < 2) { return null; };
            var EkPbKi = {};
            EkPbKi.lBONbL = String(lBONbL);
            EkPbKi.IEEIbf = dCibpa(ajJgBK.shift());
            EkPbKi.bKgEdk = [];
            cIhEIM--;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                iBamkN = ajJgBK[cJcdCM].split('^');
                if (iBamkN.length == 3) { EkPbKi.PibBHI = iBamkN.shift(); };
                if (iBamkN.length != 2) { return null; };
                PfIHKb = {};
                if (iBamkN[0] != '') { PfIHKb.gv = iBamkN[0]; };
                if (iBamkN[1] != '') { PfIHKb.gs = iBamkN[1]; };
                EkPbKi.bKgEdk.push(PfIHKb);
            };
            if (EkPbKi.PibBHI === undefined) { return null; };
            return EkPbKi;
        };
        var fLIjJE = '';
        var hCjiLE = null;
        var ccpkoK = [0, 0];
        var DdoalH = [10, 10];
        var iAhoFC = [10, 10];
        var hfkJJE = {};
        var LOnGho = {};
        EpDMcA.JDekmb = function(bKoNmi) {
            if (fLIjJE == '') { return null; };
            if (!hfkJJE) { return null; };
            if (hCjiLE) {
                var kjbpEL = hCjiLE.GigegA.GSP_Preview;
                window.removeEventListener('resize', bCeNcm, false);
                kjbpEL.removeEventListener('mousemove', FBKnEp, false);
                kjbpEL.removeEventListener('touchstart', lfNkDi, false);
                kjbpEL.removeEventListener('touchmove', lfNkDi, false);
            };
            fLIjJE = '';
            var eGpbfM = null;
            for (var aIfLkO in hfkJJE) {
                var OadMid = false;
                var jFPKaL = hfkJJE[aIfLkO].OpnceF;
                var icNiAj = hfkJJE[aIfLkO].gfCiPO;
                for (var JdinEc in jFPKaL) { if (jFPKaL[JdinEc] != icNiAj[JdinEc]) { OadMid = true; break; } };
                if (OadMid) {
                    var ICbCFD = null;
                    if (aIfLkO == 'billiards') {
                        var CjnLhN = icNiAj.CjnLhN;
                        if (CjnLhN < 100) { CjnLhN = 0; };
                        ICbCFD = { c: CjnLhN, f: icNiAj.jnfFPa, t: icNiAj.lcFaFD, b: icNiAj.Dheeik, e: icNiAj.KHfcLh };
                    } else if (aIfLkO == 'chess') { ICbCFD = { b: icNiAj.mepKMl, f: icNiAj.ebnklm, e: icNiAj.KHfcLh }; } else if (aIfLkO == 'checkers') { ICbCFD = { b: icNiAj.mepKMl, f: icNiAj.ebnklm, e: icNiAj.KHfcLh }; } else { continue; };
                    if (ICbCFD) {
                        bKoNmi.iMAmEk.options[aIfLkO] = ICbCFD;
                        if (!eGpbfM) { eGpbfM = {}; };
                        eGpbfM[aIfLkO] = ICbCFD;
                    }
                };
            };
            return eGpbfM;
        };
        EpDMcA.jLgaak = function(bKoNmi, mnmaal, dFifpA) {
            fLIjJE = mnmaal;
            hCjiLE = dFifpA;
            if (!hfkJJE[fLIjJE]) { hfkJJE[fLIjJE] = { JeMDHe: 0, OpnceF: {}, gfCiPO: {}, NAcbmL: {}, JkEjck: {} }; };
            var GigegA = hCjiLE.GigegA;
            var jFPKaL = hfkJJE[fLIjJE].OpnceF;
            var icNiAj = hfkJJE[fLIjJE].gfCiPO;
            if (bKoNmi.iMAmEk.statistics[fLIjJE]) { hfkJJE[fLIjJE].JeMDHe = dCibpa(bKoNmi.iMAmEk.statistics[fLIjJE][0]); } else { hfkJJE[fLIjJE].JeMDHe = 0; };
            var JECGfN = bKoNmi.NnAcHp.w;
            var DcjJEc = BLAZE.NeOMlH;
            var ggIang = Object.keys(JECGfN);
            var jgGOCF = ggIang.length;
            var moMiPf = AemJIe(hfkJJE[fLIjJE].JeMDHe);
            var JebkAE, iLEedm, gNcbKl, iBamkN, cJcdCM, dFifod, MnkekN;
            var kJkjGn, GBEKfi = bKoNmi.iMAmEk.options[fLIjJE];
            var FkfFah = BLAZE.CONTENT_VERSION;
            if (fLIjJE == 'billiards') {
                GigegA.gst_billiards_table_select.onchange = OBlKcb;
                GigegA.gst_billiards_bg_select.onchange = ojOBNh;
                GigegA.gst_billiards_effect_select.onchange = GEcGop;
                var kjbpEL = hCjiLE.GigegA.GSP_Preview;
                window.addEventListener('resize', bCeNcm, false);
                kjbpEL.addEventListener('mousemove', FBKnEp, false);
                kjbpEL.addEventListener('touchstart', lfNkDi, false);
                kjbpEL.addEventListener('touchmove', lfNkDi, false);
                dFifod = ggIang.join(':') + moMiPf;
                if (LOnGho[fLIjJE] !== dFifod) {
                    LOnGho[fLIjJE] = dFifod;
                    GigegA.gst_billiards_cue_select.onchange = hdIdpf;
                    dLeLMm.MDIllm(GigegA.gst_billiards_cue_select);
                    MnkekN = document.createElement('option');
                    MnkekN.value = 0;
                    MnkekN.innerHTML = IpFeae('standard_item');
                    GigegA.gst_billiards_cue_select.appendChild(MnkekN);
                    GigegA.gst_billiards_table_select.onchange = OBlKcb;
                    dLeLMm.MDIllm(GigegA.gst_billiards_table_select);
                    MnkekN = document.createElement('option');
                    MnkekN.value = 0;
                    MnkekN.innerHTML = IpFeae('standard_item');
                    GigegA.gst_billiards_table_select.appendChild(MnkekN);
                    GigegA.gst_billiards_bg_select.onchange = ojOBNh;
                    dLeLMm.MDIllm(GigegA.gst_billiards_bg_select);
                    MnkekN = document.createElement('option');
                    MnkekN.value = 0;
                    MnkekN.innerHTML = IpFeae('no_background');
                    GigegA.gst_billiards_bg_select.appendChild(MnkekN);
                    GigegA.gst_billiards_effect_select.onchange = GEcGop;
                    dLeLMm.MDIllm(GigegA.gst_billiards_effect_select);
                    MnkekN = document.createElement('option');
                    MnkekN.value = 0;
                    MnkekN.innerHTML = IpFeae('no_effect');
                    GigegA.gst_billiards_effect_select.appendChild(MnkekN);
                    dLeLMm.MDIllm(GigegA.fabric_set);
                    MnkekN = document.createElement('div');
                    MnkekN.KdFNpN = 0;
                    MnkekN.className = 'FabricSlot';
                    MnkekN.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_fabric').src + '")';
                    AchggF.BPmDoj(MnkekN, FiKdGc, [0], false);
                    GigegA.fabric_set.appendChild(MnkekN);
                    for (JebkAE = 0; JebkAE < jgGOCF; JebkAE++) {
                        iBamkN = ggIang[JebkAE];
                        if (!DcjJEc.hasOwnProperty(iBamkN)) { continue; };
                        if (DcjJEc[iBamkN].length > 1) { if (DcjJEc[iBamkN][1] !== 'gamezer') { continue; } };
                        if (iBamkN.substr(0, 4) == 'pcue') {
                            iBamkN = dCibpa(iBamkN.substr(4));
                            MnkekN = document.createElement('option');
                            MnkekN.value = iBamkN + 100;
                            MnkekN.innerHTML = IpFeae('inv_pcue' + iBamkN);
                            GigegA.gst_billiards_cue_select.appendChild(MnkekN);
                        } else if (iBamkN.substr(0, 4) == 'acue') {
                            iBamkN = dCibpa(iBamkN.substr(4));
                            MnkekN = document.createElement('option');
                            MnkekN.value = iBamkN + 1000;
                            MnkekN.innerHTML = IpFeae('inv_acue' + iBamkN);
                            GigegA.gst_billiards_cue_select.appendChild(MnkekN);
                        } else if (iBamkN.substr(0, 3) == 'ttb') {
                            iBamkN = dCibpa(iBamkN.substr(3));
                            MnkekN = document.createElement('option');
                            MnkekN.value = iBamkN;
                            MnkekN.innerHTML = IpFeae('inv_ttb' + iBamkN);
                            GigegA.gst_billiards_table_select.appendChild(MnkekN);
                        } else if (iBamkN.substr(0, 3) == 'tbg') {
                            iBamkN = dCibpa(iBamkN.substr(3));
                            MnkekN = document.createElement('option');
                            MnkekN.value = iBamkN;
                            MnkekN.innerHTML = IpFeae('inv_tbg' + iBamkN);
                            GigegA.gst_billiards_bg_select.appendChild(MnkekN);
                        } else if (iBamkN.substr(0, 2) == 'be') {
                            iBamkN = dCibpa(iBamkN.substr(2));
                            MnkekN = document.createElement('option');
                            MnkekN.value = iBamkN;
                            MnkekN.innerHTML = IpFeae('inv_be' + iBamkN);
                            GigegA.gst_billiards_effect_select.appendChild(MnkekN);
                        } else if (iBamkN.substr(0, 3) == 'fbr') {
                            iBamkN = dCibpa(iBamkN.substr(3));
                            if (iBamkN == 0) { cJcdCM = 1; } else { cJcdCM = 0; };
                            iBamkN = iBamkN * 100;
                            for (iLEedm = cJcdCM; iLEedm < 5; iLEedm++) {
                                gNcbKl = iBamkN + iLEedm;
                                MnkekN = document.createElement('div');
                                MnkekN.KdFNpN = gNcbKl;
                                MnkekN.className = 'FabricSlot';
                                MnkekN.style.backgroundImage = 'url("' + aaPJke + 'fbr' + gNcbKl + '.png?' + FkfFah + '")';
                                AchggF.BPmDoj(MnkekN, FiKdGc, [gNcbKl], false);
                                GigegA.fabric_set.appendChild(MnkekN);
                            }
                        };
                    };
                    MnkekN = document.createElement('div');
                    MnkekN.className = 'clear';
                    GigegA.fabric_set.appendChild(MnkekN);
                };
                icNiAj.CjnLhN = moMiPf;
                if (GBEKfi.c > 1000) { kJkjGn = 'acue' + (GBEKfi.c - 1000); if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.CjnLhN = GBEKfi.c; } } else if (GBEKfi.c > 100) { kJkjGn = 'pcue' + (GBEKfi.c - 100); if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.CjnLhN = GBEKfi.c; } };
                jFPKaL.CjnLhN = icNiAj.CjnLhN;
                if (icNiAj.CjnLhN < 100) { GigegA.gst_billiards_cue_select.value = 0; } else { GigegA.gst_billiards_cue_select.value = icNiAj.CjnLhN; };
                icNiAj.KHfcLh = 0;
                icNiAj.lcFaFD = 0;
                if (GBEKfi.t > 0) { kJkjGn = 'ttb' + GBEKfi.t; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.lcFaFD = GBEKfi.t; } };
                jFPKaL.lcFaFD = icNiAj.lcFaFD;
                GigegA.gst_billiards_table_select.value = icNiAj.lcFaFD;
                icNiAj.jnfFPa = 0;
                if (GBEKfi.f > 0) {
                    var lEOJAg = GBEKfi.f % 100;
                    var GBFcjM = (GBEKfi.f - lEOJAg) * 0.01;
                    kJkjGn = 'fbr' + GBFcjM;
                    if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) {
                        if (lEOJAg > 4) { lEOJAg = 4; };
                        icNiAj.jnfFPa = (GBFcjM * 100) + lEOJAg;
                    }
                };
                jFPKaL.jnfFPa = icNiAj.jnfFPa;
                icNiAj.Dheeik = 0;
                if (GBEKfi.b > 0) { kJkjGn = 'tbg' + GBEKfi.b; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.Dheeik = GBEKfi.b; } };
                jFPKaL.Dheeik = icNiAj.Dheeik;
                GigegA.gst_billiards_bg_select.value = icNiAj.Dheeik;
                icNiAj.KHfcLh = 0;
                if (GBEKfi.e > 0) { kJkjGn = 'be' + GBEKfi.e; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.KHfcLh = GBEKfi.e; } };
                jFPKaL.KHfcLh = icNiAj.KHfcLh;
                GigegA.gst_billiards_effect_select.value = icNiAj.KHfcLh;
                bCeNcm();
                FiKdGc(jFPKaL.jnfFPa)
            } else if (fLIjJE == 'chess') {
                GigegA.gst_chess_board_select.onchange = ADhbEo;
                dLeLMm.MDIllm(GigegA.gst_chess_board_select);
                MnkekN = document.createElement('option');
                MnkekN.value = 0;
                MnkekN.innerHTML = IpFeae('standard_item');
                GigegA.gst_chess_board_select.appendChild(MnkekN);
                for (JebkAE = 0; JebkAE < jgGOCF; JebkAE++) {
                    iBamkN = ggIang[JebkAE];
                    if (!DcjJEc.hasOwnProperty(iBamkN)) { continue; };
                    if (DcjJEc[iBamkN].length > 1) { if (DcjJEc[iBamkN][1] !== 'gamezer') { continue; } };
                    if (iBamkN.substr(0, 3) == 'chb') {
                        iBamkN = dCibpa(iBamkN.substr(3));
                        MnkekN = document.createElement('option');
                        MnkekN.value = iBamkN;
                        MnkekN.innerHTML = IpFeae('inv_chb' + iBamkN);
                        GigegA.gst_chess_board_select.appendChild(MnkekN);
                    } else if (iBamkN.substr(0, 3) == 'csf') {
                        iBamkN = dCibpa(iBamkN.substr(3));
                        MnkekN = document.createElement('option');
                        MnkekN.value = iBamkN;
                        MnkekN.innerHTML = IpFeae('inv_csf' + iBamkN);
                        GigegA.gst_chess_pieceset_select.appendChild(MnkekN);
                    }
                };
                icNiAj.mepKMl = 0;
                if (GBEKfi.b > 0) { kJkjGn = 'chb' + GBEKfi.b; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.mepKMl = GBEKfi.b; } };
                jFPKaL.mepKMl = icNiAj.mepKMl;
                GigegA.gst_chess_board_select.value = icNiAj.mepKMl;
                icNiAj.KHfcLh = 0;
                oONPPe();
            } else if (fLIjJE == 'checkers') {
                GigegA.gst_checkers_board_select.onchange = HpAbhd;
                dLeLMm.MDIllm(GigegA.gst_checkers_board_select);
                MnkekN = document.createElement('option');
                MnkekN.value = 0;
                MnkekN.innerHTML = IpFeae('standard_item');
                GigegA.gst_checkers_board_select.appendChild(MnkekN);
                GigegA.gst_checkers_pieceset_select.onchange = IHpFfk;
                dLeLMm.MDIllm(GigegA.gst_checkers_pieceset_select);
                MnkekN = document.createElement('option');
                MnkekN.value = 0;
                MnkekN.innerHTML = IpFeae('standard_item');
                GigegA.gst_checkers_pieceset_select.appendChild(MnkekN);
                for (JebkAE = 0; JebkAE < jgGOCF; JebkAE++) {
                    iBamkN = ggIang[JebkAE];
                    if (!DcjJEc.hasOwnProperty(iBamkN)) { continue; };
                    if (DcjJEc[iBamkN].length > 1) { if (DcjJEc[iBamkN][1] !== 'gamezer') { continue; } };
                    if (iBamkN.substr(0, 3) == 'chb') {
                        iBamkN = dCibpa(iBamkN.substr(3));
                        MnkekN = document.createElement('option');
                        MnkekN.value = iBamkN;
                        MnkekN.innerHTML = IpFeae('inv_chb' + iBamkN);
                        GigegA.gst_checkers_board_select.appendChild(MnkekN);
                    } else if (iBamkN.substr(0, 3) == 'ckf') {
                        iBamkN = dCibpa(iBamkN.substr(3));
                        MnkekN = document.createElement('option');
                        MnkekN.value = iBamkN;
                        MnkekN.innerHTML = IpFeae('inv_ckf' + iBamkN);
                        GigegA.gst_checkers_pieceset_select.appendChild(MnkekN);
                    }
                };
                icNiAj.mepKMl = 0;
                if (GBEKfi.b > 0) { kJkjGn = 'chb' + GBEKfi.b; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.mepKMl = GBEKfi.b; } };
                jFPKaL.mepKMl = icNiAj.mepKMl;
                GigegA.gst_checkers_board_select.value = icNiAj.mepKMl;
                icNiAj.ebnklm = 0;
                if (GBEKfi.f > 0) { kJkjGn = 'ckf' + GBEKfi.f; if (JECGfN.hasOwnProperty(kJkjGn) && DcjJEc.hasOwnProperty(kJkjGn)) { icNiAj.ebnklm = GBEKfi.f; } };
                jFPKaL.ebnklm = icNiAj.ebnklm;
                GigegA.gst_checkers_pieceset_select.value = icNiAj.ebnklm;
                icNiAj.KHfcLh = 0;
                oONPPe();
            }
        };

        function oONPPe() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            var GigegA = hCjiLE.GigegA;
            var icNiAj = hfkJJE[fLIjJE].gfCiPO;
            var nfmHAA = hfkJJE[fLIjJE].NAcbmL;
            var edPmlo = hfkJJE[fLIjJE].JkEjck;
            var ePoLdm;
            if (fLIjJE == 'billiards') {
                if (icNiAj.CjnLhN !== nfmHAA.CjnLhN) {
                    ePoLdm = icNiAj.CjnLhN;
                    nfmHAA.CjnLhN = ePoLdm;
                    if (ePoLdm < 100) {
                        if (ePoLdm < 1) { GigegA.GSP_Cue.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_cue').src + '")'; } else {
                            hCjiLE.classList.add('loadgsc');
                            edPmlo.CjnLhN = true;
                            ePoLdm = 'cue' + ePoLdm;
                            BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, NoknpC, 'CjnLhN');
                        }
                    } else if (ePoLdm < 1000) {
                        ePoLdm -= 100;
                        hCjiLE.classList.add('loadgsc');
                        edPmlo.CjnLhN = true;
                        ePoLdm = 'pcue' + ePoLdm;
                        BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, NoknpC, 'CjnLhN');
                    } else {
                        ePoLdm -= 1000;
                        hCjiLE.classList.add('loadgsc');
                        edPmlo.CjnLhN = true;
                        ePoLdm = 'apcue' + ePoLdm;
                        BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, NoknpC, 'CjnLhN');
                    }
                };
                if (icNiAj.lcFaFD !== nfmHAA.lcFaFD) {
                    ePoLdm = icNiAj.lcFaFD;
                    nfmHAA.lcFaFD = ePoLdm;
                    if (ePoLdm == 0) { GigegA.GSP_Table.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_table').src + '")'; } else {
                        hCjiLE.classList.add('loadgsc');
                        edPmlo.lcFaFD = true;
                        ePoLdm = 'ttb' + ePoLdm;
                        BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, NoknpC, 'lcFaFD');
                    }
                };
                if (icNiAj.jnfFPa !== nfmHAA.jnfFPa) {
                    ePoLdm = icNiAj.jnfFPa;
                    nfmHAA.jnfFPa = ePoLdm;
                    if (ePoLdm == 0) { GigegA.GSP_Fabric.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_fabric').src + '")'; } else {
                        hCjiLE.classList.add('loadgsc');
                        edPmlo.jnfFPa = true;
                        ePoLdm = 'fbr' + ePoLdm;
                        BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, NoknpC, 'jnfFPa');
                    }
                };
                if (icNiAj.Dheeik !== nfmHAA.Dheeik) { nfmHAA.Dheeik = icNiAj.Dheeik; }
            } else if (fLIjJE == 'chess') {} else if (fLIjJE == 'checkers') {}
        };

        function NoknpC(pKHmnh, NpfeFE, fogfBH) {
            if (!NpfeFE) { return; };
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            var nfmHAA = hfkJJE[fLIjJE].NAcbmL;
            var edPmlo = hfkJJE[fLIjJE].JkEjck;
            var GigegA = hCjiLE.GigegA;
            if (fogfBH == 'CjnLhN') {
                if (nfmHAA.CjnLhN != 0) {
                    edPmlo[fogfBH] = false;
                    GigegA.GSP_Cue.style.backgroundImage = 'url("' + NpfeFE.src + '")';
                }
            } else if (fogfBH == 'lcFaFD') {
                if (nfmHAA.lcFaFD != 0) {
                    edPmlo[fogfBH] = false;
                    GigegA.GSP_Table.style.backgroundImage = 'url("' + NpfeFE.src + '")';
                }
            } else if (fogfBH == 'jnfFPa') {
                if (nfmHAA.jnfFPa != 0) {
                    edPmlo[fogfBH] = false;
                    GigegA.GSP_Fabric.style.backgroundImage = 'url("' + NpfeFE.src + '")';
                }
            } else { $warn(61190395); return; };
            for (var JdinEc in edPmlo) { if (edPmlo[JdinEc]) { return; } };
            hCjiLE.classList.remove('loadgsc');
        };

        function FCgkdn(EiINbF) {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            var GigegA = hCjiLE.GigegA;
            AEOgJp.GKEMcP(EiINbF, ccpkoK);
            var kjbpEL = hCjiLE.GigegA.GSP_CueContanier;
            var obNnhC = EiINbF[0] / DdoalH[0];
            if (obNnhC < 0) { obNnhC = 0; } else if (obNnhC > 1) { obNnhC = 1; };
            GigegA.GSP_CueContanier.style.left = (390 + HiMfgN.cGgNAb(-obNnhC * (70 + iAhoFC[1] - DdoalH[0]))) + 'px'
        };

        function FBKnEp(KcMelf) { FCgkdn([KcMelf.clientX, KcMelf.clientY]); };

        function lfNkDi(KcMelf) {
            if (KcMelf.changedTouches.length < 1) { return; };
            var nJogbk = KcMelf.changedTouches[0];
            FCgkdn([nJogbk.clientX, nJogbk.clientY]);
        };

        function bCeNcm(KcMelf) {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            var GigegA = hCjiLE.GigegA;
            ccpkoK = dLeLMm.OnKbCc(GigegA.GSP_Preview);
            ccpkoK[0] -= GigegA.switcher.offsetWidth * 0.25;
            DdoalH[0] = GigegA.GSP_Preview.offsetWidth;
            DdoalH[1] = GigegA.GSP_Preview.offsetHeight;
            iAhoFC[0] = GigegA.GSP_CueContanier.offsetWidth;
            iAhoFC[1] = GigegA.GSP_CueContanier.offsetHeight;
            FCgkdn([0, 0]);
        };

        function hdIdpf() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.CjnLhN = dCibpa(hCjiLE.GigegA.gst_billiards_cue_select.value);
            oONPPe();
        };

        function OBlKcb() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.lcFaFD = dCibpa(hCjiLE.GigegA.gst_billiards_table_select.value);
            oONPPe();
        };

        function IHpFfk() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.ebnklm = dCibpa(hCjiLE.GigegA.gst_checkers_pieceset_select.value);
            oONPPe();
        };

        function ADhbEo() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.mepKMl = dCibpa(hCjiLE.GigegA.gst_chess_board_select.value);
            oONPPe();
        };

        function HpAbhd() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.mepKMl = dCibpa(hCjiLE.GigegA.gst_checkers_board_select.value);
            oONPPe();
        };

        function FiKdGc(iBamkN) {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            var GigegA = hCjiLE.GigegA;
            iBamkN = dCibpa(iBamkN);
            var khFnEl = GigegA.fabric_set.children;
            var cIhEIM = khFnEl.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var PfIHKb = khFnEl[cJcdCM]; if (PfIHKb.KdFNpN === iBamkN) { PfIHKb.classList.add('selected'); } else { PfIHKb.classList.remove('selected'); } };
            hfkJJE[fLIjJE].gfCiPO.jnfFPa = iBamkN;
            oONPPe();
        };

        function ojOBNh() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.Dheeik = dCibpa(hCjiLE.GigegA.gst_billiards_bg_select.value);
            oONPPe();
        };

        function GEcGop() {
            if (fLIjJE == '') { return; };
            if (!hCjiLE) { return; };
            if (!hCjiLE.parentNode) { return; };
            if (!hfkJJE[fLIjJE]) { return; };
            hfkJJE[fLIjJE].gfCiPO.KHfcLh = dCibpa(hCjiLE.GigegA.gst_billiards_effect_select.value);
            oONPPe();
        };

        function AemJIe(JeMDHe) { JeMDHe = dCibpa(JeMDHe) * 0.01; var CcfMbF = 0; if (JeMDHe < 5) { CcfMbF = 0; } else if (JeMDHe < 10) { CcfMbF = 1; } else if (JeMDHe < 25) { CcfMbF = 2; } else if (JeMDHe < 50) { CcfMbF = 3; } else if (JeMDHe < 100) { CcfMbF = 4; } else if (JeMDHe < 200) { CcfMbF = 5; } else if (JeMDHe < 300) { CcfMbF = 6; } else if (JeMDHe < 400) { CcfMbF = 7; } else if (JeMDHe < 500) { CcfMbF = 8; } else if (JeMDHe < 1000) { CcfMbF = 9; } else if (JeMDHe < 2000) { CcfMbF = 10; } else if (JeMDHe < 3000) { CcfMbF = 11; } else if (JeMDHe < 4000) { CcfMbF = 12; } else if (JeMDHe < 5000) { CcfMbF = 13; } else if (JeMDHe < 6000) { CcfMbF = 14; } else if (JeMDHe < 7000) { CcfMbF = 15; } else if (JeMDHe < 8000) { CcfMbF = 16; } else if (JeMDHe < 9000) { CcfMbF = 17; } else if (JeMDHe < 10000) { CcfMbF = 18; } else { CcfMbF = 19; }; return CcfMbF; };
        return aGEjAM;
    })();
    BLAZE.oeefop = oeefop;
    var MeHcPi = 0;
    var EGhJiA = (function() {
        var aaPJke = BLAZE.GetENV('PROJECT_CONTENT_URL');
        var BgGFbP = [1400, 1000];
        var keDPed = [6, 3];
        var oejMcP = -28;
        var NcFLDH = 116;
        var fPkDGh = 36;
        var LePbiJ = [94, 94];
        var Bnfnhl = 12;
        var NaOHPK = 0.15;
        var hGKBio = 0.3;
        var bjAFpk = 120;
        var aGEjAM = function(GnalKe) {
            var ijmEGj = GnalKe;
            GnalKe.aGEjAM = this;
            this.bIGpib = 0;
            this.cOPbiG = false;
            this.PAFPjb = false;
            this.COhpno = function(oNAeLc, emFjKC, gBdoHa) { return ijmEGj.COhpno(oNAeLc, emFjKC, gBdoHa); };
            this.ajgNIF = function() { ijmEGj.ajgNIF(); };
            this.jNfMiL = function(ajJgBK) { ijmEGj.jNfMiL(ajJgBK); };
            this.NBOOaE = function() { ijmEGj.NBOOaE(); };
            this.BCAKgm = function() { ijmEGj.BCAKgm(); };
            this.HjKaLb = function() { ijmEGj.HjKaLb(); };
            this.fpCIhi = function(INfAAc) { ijmEGj.fpCIhi(INfAAc); };
            this.dpneGd = function(JkgjnL) { ijmEGj.dpneGd(JkgjnL); };
            this.ICBiai = function(bekBpl) { ijmEGj.ICBiai(bekBpl); };
            this.OcDfbM = function(GhNgbO) { ijmEGj.OcDfbM(GhNgbO); };
        };
        var hJEkmd = function(MCaldm) { this.OLBcNb(MCaldm); };
        hJEkmd.prototype.OLBcNb = function(MCaldm) {
            if (MCaldm.length < 2) { $error(20819591); return; };
            if (this.JKdCgI) { $error(20819592); return; };
            if (!epCcje(MCaldm[0])) { $error(20819593); return; };
            if (MCaldm[1]) { MeHcPi = 1; } else { MeHcPi = 0; };
            this.aGEjAM = null;
            this.mKjdCO = BLAZE.DPEkhd.amlcmM();
            this.aiIcIi = false;
            this.IOnEGD();
            this.JKdCgI = MCaldm[0];
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
            this.JPfdKP = new BLAZE.aajFEA('ChessRenderer', BgGFbP[1], BgGFbP[1], 1, MeHcPi);
            this.JPfdKP.jICMmC = true;
            this.JPfdKP.iKDDhb = false;
            this.JPfdKP.gkbHnn = false;
            this.JPfdKP.hKPAKA.cncHOL = true;
            this.oOJDaI = BLAZE.DPEkhd.cFgHGM('element', 'game.chess_table');
            if (!this.oOJDaI) { $error(63950928); return; };
            dLeLMm.dHBnji(this.oOJDaI);
            this.oOJDaI.IgCMNE = true;
            var BMnhpo = this.oOJDaI.GigegA;
            var aeDnaK = BMnhpo.table_sectors;
            var cJcdCM = 0;
            for (var PIdIFL = 0; PIdIFL < 8; PIdIFL++) {
                var anNKlf = document.createElement('div');
                anNKlf.className = 'ChessTableRow';
                anNKlf.eoIjGL = this;
                aeDnaK.appendChild(anNKlf);
                for (var iFnjBg = 0; iFnjBg < 8; iFnjBg++) {
                    var PfIHKb = BLAZE.DPEkhd.LJNFJi('game.chess_sector', false);
                    PfIHKb.kCmaeC = cJcdCM;
                    anNKlf.appendChild(PfIHKb);
                    BMnhpo['s_' + cJcdCM] = PfIHKb;
                    BMnhpo['a_' + cJcdCM] = PfIHKb;
                    cJcdCM++;
                }
            };
            aeDnaK.addEventListener('touchend', this.GCgkeK, true);
            aeDnaK.addEventListener('touchstart', this.GCgkeK, true);
            aeDnaK.addEventListener('mouseup', this.GCgkeK, true);
            aeDnaK.addEventListener('mousedown', this.GCgkeK, true);
            this.OOJBGg = BLAZE.DPEkhd.cFgHGM('element', 'game.chess_select');
            this.nfMJfe = BLAZE.DPEkhd.cFgHGM('element', 'game.chess_flash');
            var mdKOEp = this;
        };
        hJEkmd.prototype.COhpno = function(oNAeLc, emFjKC, gBdoHa) {
            if (!this.JKdCgI) { $warn(2290681); return false; };
            if (this.aiIcIi) { $warn(2290682); return false; };
            if (!oNAeLc) { $warn(2290683); return false; };
            if (!emFjKC) { $warn(2290684); return false; };
            var NHDmDG = 0;
            if (gBdoHa) { NHDmDG = 1; };
            if (MeHcPi != NHDmDG) {
                MeHcPi = NHDmDG;
                this.JPfdKP.NOjeil();
                this.JPfdKP.nbIBPk();
                this.JPfdKP = new BLAZE.aajFEA('ChessRenderer', BgGFbP[1], BgGFbP[1], 1, MeHcPi);
                this.JPfdKP.jICMmC = true;
                this.JPfdKP.iKDDhb = false;
                this.JPfdKP.gkbHnn = false;
                this.JPfdKP.hKPAKA.cncHOL = true;
            };
            this.aGEjAM.bIGpib = 0;
            this.IOnEGD();
            if (emFjKC.length != 11) { $warn(64223638); return false; };
            emFjKC[2] = dCibpa(emFjKC[2]);
            emFjKC[3] = dCibpa(emFjKC[3]);
            emFjKC[4] = dCibpa(emFjKC[4]);
            emFjKC[5] = dCibpa(emFjKC[5]);
            emFjKC[6] = dCibpa(emFjKC[6]);
            emFjKC[7] = dCibpa(emFjKC[7]);
            this.oECmEe = emFjKC;
            this.AbOpkd = emFjKC[5] == 1;
            this.kmJAAO = oNAeLc;
            var GigegA = this.kmJAAO.GigegA;
            this.dfOJLM = oNAeLc.parentNode;
            if (!this.dfOJLM) { $error(95882103); return; };
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.hLngmL = GigegA.GameScoreboard;
            this.lpLlFE = GigegA.GameArea;
            this.DLchLC = GigegA.GameFullZone;
            this.lpPabJ = GigegA.GameTable;
            this.lpPabJ.appendChild(this.oOJDaI);
            this.JPfdKP.IhnhPd(this.lpPabJ);
            this.JKdCgI.aaipCF(BgGFbP, false);
            this.hGcmiD(emFjKC[7], emFjKC[8]);
            this.aiIcIi = true;
            return true;
        };
        hJEkmd.prototype.ajgNIF = function() {
            if (!this.JKdCgI) { $warn(59029918); return; };
            this.Fgbpjh(1, '');
            this.Fgbpjh(2, '');
            this.hEPkfB([]);
            this.PMiHiP();
            this.IOnEGD();
            this.aiIcIi = false;
            if (this.OOJBGg) { if (this.OOJBGg.parentNode) { this.OOJBGg.parentNode.removeChild(this.OOJBGg); } };
            if (this.nfMJfe) { if (this.nfMJfe.parentNode) { this.nfMJfe.parentNode.removeChild(this.nfMJfe); } };
            if (this.oOJDaI) { if (this.oOJDaI.parentNode) { this.oOJDaI.parentNode.removeChild(this.oOJDaI); } };
            if (this.JPfdKP) {
                this.JPfdKP.nbIBPk();
                this.JPfdKP.aMiNKa();
            };
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
        };
        hJEkmd.prototype.HjKaLb = function() {
            this.ajgNIF();
            this.JKdCgI = null;
            this.OOJBGg = null;
            this.nfMJfe = null;
            this.oOJDaI = null;
            this.JPfdKP = null;
        };
        hJEkmd.prototype.IOnEGD = function() {
            this.bpmknm = {};
            this.bpmknm._6 = [
                [
                    [-1, 0]
                ],
                [
                    [1, 0]
                ],
                [
                    [0, -1]
                ],
                [
                    [0, 1]
                ],
                [
                    [-1, -1]
                ],
                [
                    [1, 1]
                ],
                [
                    [1, -1]
                ],
                [
                    [-1, 1]
                ]
            ];
            this.bpmknm._5 = [
                [
                    [-1, 0],
                    [-2, 0],
                    [-3, 0],
                    [-4, 0],
                    [-5, 0],
                    [-6, 0],
                    [-7, 0]
                ],
                [
                    [0, -1],
                    [0, -2],
                    [0, -3],
                    [0, -4],
                    [0, -5],
                    [0, -6],
                    [0, -7]
                ],
                [
                    [1, 0],
                    [2, 0],
                    [3, 0],
                    [4, 0],
                    [5, 0],
                    [6, 0],
                    [7, 0]
                ],
                [
                    [0, 1],
                    [0, 2],
                    [0, 3],
                    [0, 4],
                    [0, 5],
                    [0, 6],
                    [0, 7]
                ],
                [
                    [-1, -1],
                    [-2, -2],
                    [-3, -3],
                    [-4, -4],
                    [-5, -5],
                    [-6, -6],
                    [-7, -7]
                ],
                [
                    [1, -1],
                    [2, -2],
                    [3, -3],
                    [4, -4],
                    [5, -5],
                    [6, -6],
                    [7, -7]
                ],
                [
                    [-1, 1],
                    [-2, 2],
                    [-3, 3],
                    [-4, 4],
                    [-5, 5],
                    [-6, 6],
                    [-7, 7]
                ],
                [
                    [1, 1],
                    [2, 2],
                    [3, 3],
                    [4, 4],
                    [5, 5],
                    [6, 6],
                    [7, 7]
                ]
            ];
            this.bpmknm._4 = [
                [
                    [-1, -1],
                    [-2, -2],
                    [-3, -3],
                    [-4, -4],
                    [-5, -5],
                    [-6, -6],
                    [-7, -7]
                ],
                [
                    [1, -1],
                    [2, -2],
                    [3, -3],
                    [4, -4],
                    [5, -5],
                    [6, -6],
                    [7, -7]
                ],
                [
                    [-1, 1],
                    [-2, 2],
                    [-3, 3],
                    [-4, 4],
                    [-5, 5],
                    [-6, 6],
                    [-7, 7]
                ],
                [
                    [1, 1],
                    [2, 2],
                    [3, 3],
                    [4, 4],
                    [5, 5],
                    [6, 6],
                    [7, 7]
                ]
            ];
            this.bpmknm._3 = [
                [
                    [-2, 1]
                ],
                [
                    [-2, -1]
                ],
                [
                    [2, -1]
                ],
                [
                    [2, 1]
                ],
                [
                    [-1, -2]
                ],
                [
                    [1, -2]
                ],
                [
                    [-1, 2]
                ],
                [
                    [1, 2]
                ]
            ];
            this.bpmknm._2 = [
                [
                    [-1, 0],
                    [-2, 0],
                    [-3, 0],
                    [-4, 0],
                    [-5, 0],
                    [-6, 0],
                    [-7, 0]
                ],
                [
                    [0, -1],
                    [0, -2],
                    [0, -3],
                    [0, -4],
                    [0, -5],
                    [0, -6],
                    [0, -7]
                ],
                [
                    [1, 0],
                    [2, 0],
                    [3, 0],
                    [4, 0],
                    [5, 0],
                    [6, 0],
                    [7, 0]
                ],
                [
                    [0, 1],
                    [0, 2],
                    [0, 3],
                    [0, 4],
                    [0, 5],
                    [0, 6],
                    [0, 7]
                ]
            ];
            this.bpmknm._1W = [
                [
                    [1, 0]
                ]
            ];
            this.bpmknm._1WF = [
                [
                    [1, 0],
                    [2, 0]
                ]
            ];
            this.bpmknm._1WC = [
                [
                    [1, -1]
                ],
                [
                    [1, 1]
                ]
            ];
            this.bpmknm._1B = [
                [
                    [-1, 0]
                ]
            ];
            this.bpmknm._1BF = [
                [
                    [-1, 0],
                    [-2, 0]
                ]
            ];
            this.bpmknm._1BC = [
                [
                    [-1, -1]
                ],
                [
                    [-1, 1]
                ]
            ];
            this.nlemFe = null;
            this.jHPcHF = false;
            this.jDPhKk = 0;
            this.GBnioj = '';
            this.oECmEe = null;
            this.AbOpkd = false;
            this.IfHNmH = { _1: [], _2: [] };
            this.gaIpJE = [];
            this.ADeOCF = [];
            this.cpHPfC = 1.0;
            this.hgbGol = null;
            this.fjdCgI = 0;
            this.BcKPJA = 0;
            this.gAOEgM = false;
            this.fHNDkc = 0;
            this.nKdkCL = 0;
            this.kOcLKF = null;
            this.BgCLbl = [];
            this.hkLMbI = [];
            this.OdghkO = [];
            this.jDChHC = -1;
            this.NdeLeg = '';
            this.GhMInF = '';
            this.ceNmop = null;
            this.eGADpE = null;
            this.FIeFfN = {};
            this.JAcmEK = {};
            this.bhlHJO = null;
            this.ejAHOl = {};
            this.nAilaH = '';
            this.nloDdm = null;
            this.OFPgOl = false;
            this.DnGDMp = 0;
            this.BIAnlc = -1;
            this.gIklBa = [];
            this.AJBHGO = null;
            this.acaemD = '';
            this.cOhCGk = -1;
            this.jemKaO = null;
            this.HPiFCa = null;
            this.bJiMEP = 0;
            this.GfihNB = 0;
            this.mHolDN = 0;
            this.IEeIMH = 0;
            this.aKbblp = null;
            this.McLJef = 0;
            this.dNNHfe = false;
        };
        hJEkmd.prototype.dpneGd = function(JkgjnL) {
            if (!this.aiIcIi) { return; };
            if (this.oOJDaI) {
                var gNcbKl = this.oOJDaI.GigegA;
                var hKPAKA = gNcbKl.BHLoEL;
                if (!hKPAKA) {
                    hKPAKA = gNcbKl.table_super_game;
                    if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                    this.lpPabJ.appendChild(hKPAKA);
                    gNcbKl.BHLoEL = hKPAKA;
                };
                var gNcbKl = this.oOJDaI.GigegA;
                gNcbKl.table_super_game_zp.innerHTML = JkgjnL + ' ZP';
                hKPAKA.classList.add('AnimSuperGame');
            }
        };
        hJEkmd.prototype.OcDfbM = function(bJhmlj) {
            if (!this.aiIcIi) { return; };
            var EjJIlL, iBamkN, GhNgbO;
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.PacccC = dLeLMm.OnKbCc(this.BcoPPH);
            bJhmlj[0] -= bJhmlj[0] % 8;
            bJhmlj[1] -= bJhmlj[1] % 8;
            var hEdBhi = bJhmlj[0] + 'px';
            var EjbkCN = bJhmlj[1] + 'px';
            var oKcDNc = '';
            var BkKhgB = '';
            var pMAMeL = '';
            var eDGEAM = bJhmlj[0] >= bJhmlj[1];
            if (eDGEAM) {
                oKcDNc = bJhmlj[1] + 'px';
                BkKhgB = '0px';
                pMAMeL = Math.round((bJhmlj[0] - bJhmlj[1]) * 0.5) + 'px';
                this.cpHPfC = bJhmlj[0] / BgGFbP[0];
            } else {
                oKcDNc = bJhmlj[0] + 'px';
                BkKhgB = Math.round((bJhmlj[1] - bJhmlj[0]) * 0.5) + 'px';
                pMAMeL = '0px';
                this.cpHPfC = bJhmlj[1] / BgGFbP[0];
            };
            var s, l;
            if (this.oOJDaI) {
                s = this.oOJDaI.style;
                s.width = s.height = oKcDNc;
                s.top = BkKhgB;
                s.left = pMAMeL;
                var BMnhpo = this.oOJDaI.GigegA;
                BMnhpo.table_sectors.style.padding = Math.round(fPkDGh * this.cpHPfC) + 'px';
                var CdjeMc = 0.85;
                var mDAbnB = this.cpHPfC * CdjeMc;
                var haACNG = Math.round((BgGFbP[0] - BgGFbP[1]) * 0.5);
                var eeGObG, HkPNDK, fdDaBe;
                if (eDGEAM) {
                    eeGObG = Math.round(haACNG / CdjeMc) + 'px';
                    HkPNDK = Math.round(BgGFbP[1] / CdjeMc) + 'px';
                } else {
                    eeGObG = Math.round(BgGFbP[1] / CdjeMc) + 'px';
                    HkPNDK = Math.round(haACNG / CdjeMc) + 'px';
                };
                l = BMnhpo.stack_2.classList;
                s = BMnhpo.stack_2.style;
                s.width = eeGObG;
                s.height = HkPNDK;
                if (eDGEAM) {
                    l.remove('StackPortrait');
                    l.add('StackLandscape');
                    s.top = '0px';
                    s.left = '-' + eeGObG;
                    dLeLMm.KEEcac(BMnhpo.stack_2, mDAbnB, mDAbnB);
                } else {
                    l.add('StackPortrait');
                    l.remove('StackLandscape');
                    s.top = '0px';
                    s.left = '0px';
                    dLeLMm.KEEcac(BMnhpo.stack_2, mDAbnB, -mDAbnB);
                };
                l = BMnhpo.stack_1.classList;
                s = BMnhpo.stack_1.style;
                s.width = eeGObG;
                s.height = HkPNDK;
                if (eDGEAM) {
                    l.remove('StackPortrait');
                    l.add('StackLandscape');
                    s.top = '0px';
                    s.bottom = '';
                    s.left = '';
                    s.right = '-' + eeGObG;
                } else {
                    l.add('StackPortrait');
                    l.remove('StackLandscape');
                    s.top = '';
                    s.bottom = '-' + HkPNDK;
                    s.left = '0px';
                    s.right = '';
                };
                dLeLMm.KEEcac(BMnhpo.stack_1, mDAbnB, mDAbnB);
            };
            if (this.JPfdKP) {
                s = this.JPfdKP.hKPAKA.style;
                s.width = s.height = oKcDNc;
                s.top = BkKhgB;
                s.left = pMAMeL;
            };
            this.OepnhE();
        };
        hJEkmd.prototype.jNfMiL = function(ajJgBK) {
            if (!ajJgBK) { return; };
            this.jHPcHF = false;
            this.nlemFe = ajJgBK;
            this.nlemFe.OcMDpE = 0;
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.hgbGol = window.setTimeout(this.bIdfjh, 50, this);
        };
        hJEkmd.prototype.NBOOaE = function() {
            if (!this.nlemFe) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.JKdCgI.aFDeff();
            this.jHPcHF = false;
            this.nlemFe.OcMDpE = 0;
            this.hgbGol = window.setTimeout(this.bIdfjh, 50, this);
        };
        hJEkmd.prototype.GilbBF = function() {
            if (!this.nlemFe) { return; };
            if (this.nlemFe.OcMDpE >= this.nlemFe.bKgEdk.length - 1) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.jHPcHF = true;
            this.JKdCgI.jfBhKJ();
            this.JKdCgI.aFOEfh();
            this.JKdCgI.OEOpEB();
        };
        hJEkmd.prototype.BCAKgm = function() {
            if (!this.nlemFe) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.jHPcHF = false;
            this.JKdCgI.BBFIek();
            this.GEGNag();
        };
        hJEkmd.prototype.GEGNag = function() {
            if (!this.nlemFe) { return; };
            if (this.OFPgOl || this.jHPcHF) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            var aaONaI = 1500;
            if (this.nlemFe.OcMDpE < 1) { aaONaI = 50; };
            this.hgbGol = window.setTimeout(this.phHGmj, aaONaI, this);
        };
        hJEkmd.prototype.bIdfjh = function(fkiijB) {
            if (!fkiijB.nlemFe || !fkiijB.aiIcIi) { return; };
            fkiijB.pDhCiA();
        };
        hJEkmd.prototype.phHGmj = function(fkiijB) {
            if (!fkiijB.nlemFe || !fkiijB.aiIcIi) { return; };
            if (this.OFPgOl || this.jHPcHF) { return; };
            var OcMDpE = fkiijB.nlemFe.OcMDpE;
            var bKgEdk = fkiijB.nlemFe.bKgEdk;
            if (OcMDpE < bKgEdk.length) {
                var PfIHKb = bKgEdk[OcMDpE];
                OcMDpE = OcMDpE + 1;
                fkiijB.nlemFe.OcMDpE = OcMDpE;
                fkiijB.fpCIhi(PfIHKb);
            } else { fkiijB.JKdCgI.BBFIek(); }
        };
        hJEkmd.prototype.pDhCiA = function() {
            if (!this.aiIcIi) { return; };
            var iBamkN, EjJIlL, cJcdCM, cIhEIM, ilcBeA, ajJgBK, bBOchF;
            var EmNmnC = false;
            if (this.gaIpJE.length > 0) {
                ajJgBK = this.gaIpJE.shift();
                bBOchF = ajJgBK[0];
                if (bBOchF == 'i') {
                    this.GBnioj = ajJgBK[1];
                    this.JKdCgI.cBIfjo();
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.OFPgOl = false;
                    this.gIklBa = [];
                    EmNmnC = true;
                    this.DeKAaj();
                } else if (bBOchF == 's') {
                    iBamkN = ajJgBK[1].split(',');
                    if (iBamkN.length == 2) {
                        EjJIlL = dCibpa(iBamkN[0]);
                        this.ceNmop = BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_figures_' + EjJIlL);
                        if (EjJIlL == 0) { this.NdeLeg = 'chks_0_'; } else { this.NdeLeg = 'chss_' + EjJIlL + '_'; };
                        EjJIlL = dCibpa(iBamkN[1]);
                        this.eGADpE = BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_figures_' + EjJIlL);
                        if (EjJIlL == 0) { this.GhMInF = 'chks_0_'; } else { this.GhMInF = 'chss_' + EjJIlL + '_'; }
                    };
                    if (this.OFPgOl) { this.nAilaH = ajJgBK[2]; } else { this.HBBBbi(ajJgBK[2]); }
                } else if (bBOchF == 'a') {
                    this.BcKPJA = dCibpa(ajJgBK[2]);
                    this.fjdCgI = dCibpa(ajJgBK[1]);
                    this.gAOEgM = false;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.ejAHOl = {};
                    this.JKdCgI.bLbBKB();
                    this.hkLMbI = [];
                    if (ajJgBK[3] != '') {
                        ilcBeA = ajJgBK[3].split(',');
                        cIhEIM = ilcBeA.length;
                        for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { EjJIlL = ilcBeA[cJcdCM].split('_'); if (EjJIlL.length == 3) { this.hkLMbI.push([dCibpa(EjJIlL[0]), dCibpa(EjJIlL[1]), dCibpa(EjJIlL[2])]); } };
                    };
                    this.OdghkO = [];
                    if (ajJgBK[4] != '') {
                        ilcBeA = ajJgBK[4].split(',');
                        cIhEIM = ilcBeA.length;
                        for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { this.OdghkO['_' + ilcBeA[cJcdCM]] = true; }
                    };
                } else if (bBOchF == 'r') {
                    this.gAOEgM = false;
                    this.fjdCgI = 0;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.ejAHOl = {};
                    this.JKdCgI.BNkojA();
                } else if (bBOchF == 'p') {
                    var LePFnj = dCibpa(ajJgBK[1]);
                    if ((this.aGEjAM.bIGpib != LePFnj && LePFnj > 0) || !this.aGEjAM.cOPbiG) {
                        this.BcKPJA = dCibpa(ajJgBK[3]);
                        var LNfmCG = [
                            [dCibpa(ajJgBK[2]), dCibpa(ajJgBK[4].split(':')[0])]
                        ];
                        if (ajJgBK[5] != '') { ilcBeA = ajJgBK[5].split('_'); if (ilcBeA.length == 2) { LNfmCG.push([dCibpa(ilcBeA[0]), dCibpa(ilcBeA[1]), true]); } };
                        this.ckIaEI(LNfmCG);
                    }
                } else { $warn('GC ' + bBOchF); }
            };
            if (this.ADeOCF.length > 0 && !EmNmnC) {
                this.JKdCgI.aFDeff();
                var ePoLdm = this.ADeOCF.shift();
                var NlPIck = HiMfgN.dcahnC(MmFnAP() - ePoLdm[0]);
                ajJgBK = ePoLdm[1];
                var cIhEIM = ajJgBK.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    iBamkN = ajJgBK[cJcdCM].split('#');
                    bBOchF = iBamkN[0];
                    if (bBOchF == 'p') { if (iBamkN.length < 4) { this.JKdCgI.HhlhKD(iBamkN[1], IpFeae('computer_player'), iBamkN[3]); } else { this.JKdCgI.HhlhKD(iBamkN[1], iBamkN[2], iBamkN[3]); } } else if (bBOchF == 's') {} else if (bBOchF == 'i') { this.JKdCgI.laipPe(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'h') { this.Fgbpjh(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'j') { this.peaOmi(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'c') { this.JKdCgI.PHafCn(iBamkN[1]); } else if (bBOchF == 't') { this.JKdCgI.abgdOj(dCibpa(iBamkN[1]) + NlPIck, iBamkN[2]); } else if (bBOchF == 'e') { this.JKdCgI.iClGgO(iBamkN[1]); } else if (bBOchF == 'r') { this.JKdCgI.FkCIHc(iBamkN[1], dCibpa(iBamkN[2]) + NlPIck); } else if (bBOchF == 'w') {
                        this.JKdCgI.OEOpEB();
                        if (this.OFPgOl) { this.nloDdm = iBamkN; } else {
                            this.gAOEgM = false;
                            this.fjdCgI = 0;
                            this.fHNDkc = 0;
                            this.nKdkCL = 0;
                            this.hEPkfB([]);
                            this.PMiHiP();
                            this.bhlHJO = null;
                            this.ejAHOl = {};
                            this.JKdCgI.OEOpEB();
                            this.JKdCgI.JAdFJk(iBamkN[1], iBamkN[2], iBamkN[3], iBamkN[4], iBamkN[5], iBamkN[6]);
                            this.nloDdm = null;
                        }
                    } else if (bBOchF == 'v') { this.JKdCgI.fNCPnN(); var eDLbgB = iBamkN.length; for (var EnibFl = 1; EnibFl < eDLbgB; EnibFl++) { this.JKdCgI.nabEiA(iBamkN[EnibFl]); } } else if (bBOchF == 'l') { this.JKdCgI.nabEiA(iBamkN[1]); } else { $warn('IC ' + bBOchF); }
                };
            };
            if (this.gaIpJE.length > 0 || this.ADeOCF.length > 0) { this.pDhCiA(); } else if (this.nlemFe) { this.GEGNag(); }
        };
        hJEkmd.prototype.fpCIhi = function(INfAAc) {
            if (!this.aiIcIi) { return; };
            if (!INfAAc) { return; };
            if (INfAAc.hasOwnProperty('gcn')) { this.JKdCgI.dFbJkH(); };
            if (INfAAc.hasOwnProperty('cpi')) { this.aGEjAM.bIGpib = dCibpa(INfAAc['cpi']); };
            var gFiOmG = false;
            if (INfAAc.hasOwnProperty('gv')) {
                gFiOmG = true;
                var khFnEl = String(INfAAc.gv).split('|');
                var cIhEIM = khFnEl.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    var IDKdaa = khFnEl[cJcdCM].split('#');
                    var EEkoKP = IDKdaa[0];
                    this.gaIpJE.push(IDKdaa);
                }
            };
            if (INfAAc.hasOwnProperty('gs')) {
                gFiOmG = true;
                this.ADeOCF.push([MmFnAP(), String(INfAAc.gs).split('|')]);
            };
            if (!this.ccehkL && gFiOmG) { this.pDhCiA(); }
        };
        hJEkmd.prototype.ICBiai = function(bekBpl) {
            if (!this.aiIcIi) { return; };
            this.BAAkAa();
        };
        hJEkmd.prototype.hGcmiD = function(MhGMlH, NADDee) {
            MhGMlH = dCibpa(MhGMlH);
            NADDee = dCibpa(NADDee);
            this.jDPhKk = kPpOoh();
            this.JPfdKP.NOjeil();
            this.JAcmEK = {};
            var BMnhpo = this.oOJDaI.GigegA;
            BMnhpo.table_default.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_default_table').src + '")';
            BMnhpo.table_overlay.classList.remove('transition');
            BMnhpo.table_overlay.style.backgroundImage = 'none';
            if (MhGMlH > 0) {
                BMnhpo.table_overlay.style.display = 'block';
                BMnhpo.table_overlay.style.opacity = '0';
                var ePoLdm = 'chb' + MhGMlH;
                BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, this.Lphbgg, this);
            } else { BMnhpo.table_overlay.style.display = 'none'; }
        };
        hJEkmd.prototype.hHGnAN = function() { return (kPpOoh() - this.jDPhKk) < 1000; };
        hJEkmd.prototype.Lphbgg = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki || !NpfeFE) { return; };
            if (!hGbOki.oOJDaI) { return; };
            var hKPAKA = hGbOki.oOJDaI.GigegA.table_overlay;
            hKPAKA.style.backgroundImage = 'url("' + NpfeFE.src + '")';
            if (!hGbOki.hHGnAN()) { hKPAKA.classList.add('transition'); };
            hKPAKA.style.opacity = '1';
        };
        hJEkmd.prototype.HBBBbi = function(hAkImK) {
            this.bhlHJO = null;
            this.ejAHOl = {};
            this.nAilaH = '';
            if (!this.aiIcIi) { return; };
            if (!this.oOJDaI) { return; };
            var BMnhpo = this.oOJDaI.GigegA;
            if (this.jDChHC != this.aGEjAM.bIGpib) {
                this.jDChHC = this.aGEjAM.bIGpib;
                if (this.jDChHC == 1 || this.jDChHC == 2) {
                    BMnhpo.table_base.classList.remove('FlipBoard');
                    BMnhpo.table_numbers.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_numbers_' + this.jDChHC).src + '")';
                } else {
                    BMnhpo.table_base.classList.add('FlipBoard');
                    BMnhpo.table_numbers.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_numbers_0').src + '")';
                };
                var iBamkN;
                var aeDnaK = BMnhpo.table_sectors;
                for (var cJcdCM = 0; cJcdCM < 64; cJcdCM++) {
                    var PfIHKb = BMnhpo['s_' + cJcdCM];
                    var kCmaeC = cJcdCM;
                    var MlnmKA = kCmaeC % 8;
                    var HloEke = (kCmaeC - MlnmKA) / 8;
                    if (this.jDChHC == 1) {
                        iBamkN = HloEke;
                        HloEke = MlnmKA;
                        MlnmKA = 7 - iBamkN;
                    } else if (this.jDChHC == 2) {
                        iBamkN = HloEke;
                        HloEke = 7 - MlnmKA;
                        MlnmKA = iBamkN;
                    };
                    kCmaeC = HloEke * 8 + MlnmKA;
                    BMnhpo['a_' + kCmaeC] = PfIHKb;
                }
            };
            this.hEPkfB([]);
            this.PMiHiP();
            this.OFPgOl = false;
            this.gIklBa = [];
            var aiBFbb = Object.keys(this.FIeFfN);
            this.FIeFfN = {};
            var khFnEl = hAkImK.split(';');
            var lNcFiD, ilcBeA, cJcdCM, cIhEIM = khFnEl.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { ilcBeA = khFnEl[cJcdCM].split(':'); if (ilcBeA.length == 2) { this.FIeFfN['_' + dCibpa(ilcBeA[0])] = [dCibpa(ilcBeA[1]), 0]; } else if (ilcBeA.length == 3) { this.FIeFfN['_' + dCibpa(ilcBeA[0])] = [dCibpa(ilcBeA[1]), dCibpa(ilcBeA[2])]; } };
            var fiebnJ = '';
            var gNcbKl = aiBFbb.length;
            for (cJcdCM = 0; cJcdCM < gNcbKl; cJcdCM++) { lNcFiD = aiBFbb[cJcdCM]; if (!this.FIeFfN[lNcFiD]) { ilcBeA = dCibpa(lNcFiD.substring(1)); if (ilcBeA >= 1 && ilcBeA <= 8) { fiebnJ = this.GhMInF; } else if (ilcBeA >= 21 && ilcBeA <= 28) { fiebnJ = this.NdeLeg; } }; };
            if (fiebnJ != '') { if (this.aiIcIi && this.oOJDaI && cIhEIM > 0) { LLFKph.LKkafb(fiebnJ + 'kill', 1, false, 0, true); } };
            this.OepnhE();
            this.BIOhpL(1);
            this.BIOhpL(2);
        };
        hJEkmd.prototype.DeKAaj = function() {
            this.FIeFfN = {};
            this.OepnhE();
        };
        hJEkmd.prototype.OepnhE = function() {
            if (!this.aiIcIi) { return; };
            if (!this.oOJDaI) { return; };
            if (this.jDChHC < 0) { return; };
            var KgDnNJ, aCHjkF;
            for (KgDnNJ in this.FIeFfN) {
                var aCHjkF = dCibpa(KgDnNJ.substring(1));
                var jMDjil = aCHjkF < 21;
                var hKPAKA = this.JAcmEK[KgDnNJ];
                if (!hKPAKA) {
                    if (jMDjil) {
                        hKPAKA = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                        hKPAKA.hMfInb = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                    } else {
                        hKPAKA = new BLAZE.pEMpHD(this.eGADpE, 1, 4, keDPed);
                        hKPAKA.hMfInb = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                    };
                    hKPAKA.lnJkFm(-1, hKPAKA.hMfInb);
                    this.JPfdKP.lnJkFm(-1, hKPAKA);
                    this.JAcmEK[KgDnNJ] = hKPAKA;
                };
                var lBkFfl = aCHjkF % 20;
                if (this.FIeFfN[KgDnNJ][1] > 0) { lBkFfl = 15; };
                if (lBkFfl == 16) { lBkFfl = 0; } else if (lBkFfl == 15) { lBkFfl = 1; } else if (lBkFfl >= 13) { lBkFfl = 2; } else if (lBkFfl >= 11) { lBkFfl = 3; } else if (lBkFfl >= 9) { lBkFfl = 4; } else { lBkFfl = 5; };
                hKPAKA.hMfInb.OmMiOf(lBkFfl + 12);
                if (!jMDjil) { lBkFfl = lBkFfl + 6; };
                hKPAKA.OmMiOf(lBkFfl);
                AEOgJp.MOGook(this.JdBDaN(this.FIeFfN[KgDnNJ][0]), this.JAcmEK[KgDnNJ].ooLIDD);
            };
            var fgEAcn = Object.keys(this.JAcmEK);
            var cIhEIM = fgEAcn.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                KgDnNJ = fgEAcn[cJcdCM];
                if (!this.FIeFfN.hasOwnProperty(KgDnNJ)) {
                    this.JPfdKP.ChmIdn(this.JAcmEK[KgDnNJ]);
                    delete this.JAcmEK[KgDnNJ];
                }
            };
            this.JPfdKP.jeEAJP();
        };
        hJEkmd.prototype.HKloFm = function(ooLIDD) {
            var iBamkN;
            var MlnmKA = Math.round(Math.floor(ooLIDD[0] / NcFLDH));
            var HloEke = Math.round(Math.floor(ooLIDD[1] / NcFLDH));
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            return [MlnmKA, HloEke];
        };
        hJEkmd.prototype.ofFoOg = function(ooLIDD) {
            var iBamkN;
            var MlnmKA = Math.round(Math.floor(ooLIDD[0] / NcFLDH));
            var HloEke = Math.round(Math.floor(ooLIDD[1] / NcFLDH));
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            return Math.round(MlnmKA + (HloEke * 8));
        };
        hJEkmd.prototype.cDHGgP = function(kCmaeC) { var MlnmKA = kCmaeC % 8; var HloEke = (kCmaeC - MlnmKA) / 8; return [MlnmKA, HloEke]; };
        hJEkmd.prototype.JdBDaN = function(kCmaeC) {
            var iBamkN;
            var MlnmKA = kCmaeC % 8;
            var HloEke = (kCmaeC - MlnmKA) / 8;
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            };
            return [(MlnmKA * NcFLDH) + LePbiJ[0], (HloEke * NcFLDH) + LePbiJ[1] + oejMcP];
        };
        hJEkmd.prototype.LBkPnh = function(kCmaeC) { var MlnmKA = kCmaeC % 8; var HloEke = (kCmaeC - MlnmKA) / 8; if (HloEke % 2 == 0) { return MlnmKA % 2 != 0; } else { return MlnmKA % 2 == 0; } };
        hJEkmd.prototype.Fgbpjh = function(mcMdAB, ajJgBK) {
            if (!this.oOJDaI) { return; };
            if (mcMdAB != 1 && mcMdAB != 2) { return; };
            this.IfHNmH['_' + mcMdAB] = [];
            this.peaOmi(mcMdAB, ajJgBK);
        };
        hJEkmd.prototype.peaOmi = function(mcMdAB, ajJgBK) {
            if (!this.oOJDaI) { return; };
            if (mcMdAB != 1 && mcMdAB != 2) { return; };
            var cjIeal = this.IfHNmH['_' + mcMdAB];
            var ilcBeA = ajJgBK.split(':');
            var cIhEIM = ilcBeA.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var iBamkN = ilcBeA[cJcdCM].split('.'); if (iBamkN.length == 2) { cjIeal.push([dCibpa(iBamkN[0]), dCibpa(iBamkN[1])]); } };
            this.BIOhpL(mcMdAB);
        };
        hJEkmd.prototype.BIOhpL = function(mcMdAB) {
            if (!this.oOJDaI) { return; };
            if (!this.ceNmop || !this.eGADpE) { return; };
            var kmJAAO;
            var djCpJK = '';
            if (this.jDChHC == 1) {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else { return; }
            } else if (this.jDChHC == 2) {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else { return; }
            } else {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else { return; }
            };
            var cjIeal = this.IfHNmH['_' + mcMdAB];
            var hKPAKA, cIhEIM = cjIeal.length;
            for (var cJcdCM = 0; cJcdCM < Bnfnhl; cJcdCM++) {
                var hnMkjD = 'S' + cJcdCM;
                var GHcmme = 'E' + cJcdCM;
                if (cJcdCM >= cIhEIM) {
                    hKPAKA = kmJAAO[GHcmme];
                    if (hKPAKA) {
                        if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                        hKPAKA = null;
                        delete kmJAAO[GHcmme];
                    };
                    hKPAKA = kmJAAO[hnMkjD];
                    if (hKPAKA) {
                        if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                        hKPAKA = null;
                        delete kmJAAO[hnMkjD];
                    }
                } else {
                    var iBamkN = cjIeal[cJcdCM];
                    var jMDjil = iBamkN[0] < 21;
                    var lBkFfl = iBamkN[0] % 20;
                    if (iBamkN[1] > 0) { lBkFfl = 15; };
                    if (lBkFfl == 16) { lBkFfl = 0; } else if (lBkFfl == 15) { lBkFfl = 1; } else if (lBkFfl >= 13) { lBkFfl = 2; } else if (lBkFfl >= 11) { lBkFfl = 3; } else if (lBkFfl >= 9) { lBkFfl = 4; } else { lBkFfl = 5; };
                    hKPAKA = kmJAAO[hnMkjD];
                    if (!hKPAKA) {
                        hKPAKA = document.createElement('div');
                        kmJAAO[hnMkjD] = hKPAKA;
                        kmJAAO.appendChild(hKPAKA);
                    };
                    hKPAKA.style.backgroundImage = djCpJK;
                    hKPAKA.className = 'ChessShadow Frame' + (lBkFfl + 12);
                    hKPAKA = kmJAAO[GHcmme];
                    if (!hKPAKA) {
                        hKPAKA = document.createElement('div');
                        kmJAAO[GHcmme] = hKPAKA;
                        kmJAAO[hnMkjD].appendChild(hKPAKA);
                    };
                    hKPAKA.style.backgroundImage = djCpJK;
                    if (jMDjil) { hKPAKA.className = 'ChessFigure Frame' + lBkFfl; } else { hKPAKA.className = 'ChessFigure Frame' + (lBkFfl + 6); }
                };
            }
        };
        hJEkmd.prototype.aPiOCB = function(kCmaeC) {
            if (!this.oOJDaI || !this.OOJBGg) { return; };
            this.PMiHiP();
            if (this.OOJBGg.parentNode) { this.OOJBGg.parentNode.removeChild(this.OOJBGg); };
            this.OOJBGg.classList.remove('Transition');
            this.OOJBGg.style.opacity = 1;
            var BMnhpo = this.oOJDaI.GigegA;
            var JdinEc = 'a_' + kCmaeC;
            if (!BMnhpo[JdinEc]) { return; };
            BMnhpo[JdinEc].appendChild(this.OOJBGg);
        };
        hJEkmd.prototype.PMiHiP = function() {
            if (this.OOJBGg) {
                this.OOJBGg.classList.add('Transition');
                this.OOJBGg.style.opacity = 0;
            }
        };
        hJEkmd.prototype.PeMPlE = function(kCmaeC) {
            if (!this.oOJDaI || !this.nfMJfe) { return; };
            if (this.nfMJfe.parentNode) { this.nfMJfe.parentNode.removeChild(this.nfMJfe); };
            var BMnhpo = this.oOJDaI.GigegA;
            var JdinEc = 'a_' + kCmaeC;
            if (!BMnhpo[JdinEc]) { return; };
            BMnhpo[JdinEc].appendChild(this.nfMJfe);
            this.nfMJfe.style.display = 'none';
            this.nfMJfe.classList.remove('Animation');
            this.nfMJfe.style.display = '';
            this.nfMJfe.classList.add('Animation');
        };
        hJEkmd.prototype.hEPkfB = function(aeDnaK) {
            if (!this.oOJDaI) { return; };
            var BMnhpo = this.oOJDaI.GigegA;
            var miChPH = {};
            var cJcdCM, cIhEIM = aeDnaK.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { miChPH['_' + aeDnaK[cJcdCM]] = true; };
            for (cJcdCM = 0; cJcdCM < 64; cJcdCM++) {
                var PfIHKb = BMnhpo['a_' + cJcdCM];
                if (PfIHKb) {
                    if (miChPH['_' + cJcdCM]) { if (this.LBkPnh(cJcdCM)) { PfIHKb.classList.add('CH_White'); } else { PfIHKb.classList.add('CH_Black'); } } else {
                        PfIHKb.classList.remove('CH_Black');
                        PfIHKb.classList.remove('CH_White');
                    }
                };
            }
        };
        hJEkmd.prototype.haAnCH = function(aCHjkF, DJMeFO) {
            if (!DJMeFO) { return; };
            if (!this.aiIcIi) { return; };
            var gceHgN = [];
            var cIhEIM = DJMeFO.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { gceHgN.push([aCHjkF, dCibpa(DJMeFO[cJcdCM])]); };
            this.ckIaEI(gceHgN);
        };
        hJEkmd.prototype.ckIaEI = function(gceHgN) {
            if (!gceHgN) { return; };
            if (!this.aiIcIi) { return; };
            if (this.OFPgOl) {
                var cIhEIM = this.gIklBa.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var hegNOA = this.gIklBa[cJcdCM]; var KgDnNJ = '_' + hegNOA[0]; var fNbdEN = dCibpa(hegNOA[1]) % 64; if (this.JAcmEK[KgDnNJ]) { this.JAcmEK[KgDnNJ].ooLIDD = this.JdBDaN(fNbdEN); } };
                this.JPfdKP.jeEAJP();
            };
            this.OFPgOl = true;
            this.gIklBa = gceHgN;
            this.njcLkJ();
        };
        hJEkmd.prototype.njcLkJ = function() {
            if (!this.aiIcIi || !this.OFPgOl) { return; };
            var JLJeih;
            if (this.acaemD != '') {
                if (this.JAcmEK[this.acaemD]) {
                    this.JPfdKP.ChmIdn(this.JAcmEK[this.acaemD]);
                    delete this.JAcmEK[this.acaemD];
                };
                this.acaemD = '';
            };
            if (this.BIAnlc > 20) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
            if (this.BIAnlc > 0) { if (this.dNNHfe) { LLFKph.LKkafb(JLJeih + 'hit', 1, false, 0, true); } };
            if (this.gIklBa.length < 1) {
                if (this.AJBHGO) {
                    this.JPfdKP.LINLfa();
                    this.JPfdKP.BFGEhp();
                    this.AJBHGO.hMfInb.hIHeHD = true;
                    this.AJBHGO = null;
                };
                this.BIAnlc = -1;
                this.OFPgOl = false;
                if (this.nAilaH != '') { this.HBBBbi(this.nAilaH); } else { this.JPfdKP.jeEAJP(); };
                if (this.gAOEgM) { if (this.kOcLKF) { if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); } }; };
                if (this.nloDdm) {
                    this.gAOEgM = false;
                    this.fjdCgI = 0;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.ejAHOl = {};
                    this.JKdCgI.OEOpEB();
                    this.JKdCgI.JAdFJk(this.nloDdm[1], this.nloDdm[2], this.nloDdm[3], this.nloDdm[4], this.nloDdm[5], this.nloDdm[6]);
                    this.nloDdm = null;
                };
                if (this.nlemFe) { this.GEGNag(); }
            } else {
                var hegNOA = this.gIklBa.shift();
                var KgDnNJ = '_' + hegNOA[0];
                var fNbdEN = dCibpa(hegNOA[1]) % 64;
                if (this.JAcmEK[KgDnNJ]) {
                    if (!this.gAOEgM) { this.PeMPlE(fNbdEN); };
                    this.OFPgOl = true;
                    this.BIAnlc = hegNOA[0];
                    this.acaemD = '';
                    this.AJBHGO = this.JAcmEK[KgDnNJ];
                    this.cOhCGk = fNbdEN;
                    this.HPiFCa = this.JdBDaN(fNbdEN);
                    this.jemKaO = AEOgJp.clhoEK(this.AJBHGO.ooLIDD);
                    this.aKbblp = AEOgJp.GajdDk(this.HPiFCa, this.jemKaO);
                    this.bJiMEP = AEOgJp.FkDjcj(this.aKbblp);
                    this.GfihNB = this.bJiMEP * 0.5;
                    this.McLJef = 1 / this.GfihNB / this.GfihNB;
                    this.mHolDN = 0;
                    this.IEeIMH = 0;
                    if (hegNOA.length > 2) { this.dNNHfe = true; } else {
                        this.dNNHfe = this.BIAnlc % 20;
                        this.dNNHfe = this.dNNHfe == 11 || this.dNNHfe == 12;
                    };
                    if (this.bJiMEP / NcFLDH > 1.9) { this.DnGDMp = hGKBio; } else { this.DnGDMp = NaOHPK; };
                    var cJcdCM, FKfcOk;
                    var cPJhlM = {};
                    for (var fKjeoh in this.FIeFfN) { if (this.FIeFfN[fKjeoh][0] == fNbdEN) { this.acaemD = fKjeoh; break; } };
                    if (this.BIAnlc > 20) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
                    this.JPfdKP.adBDen(this.AJBHGO);
                    if (this.dNNHfe) { this.AJBHGO.hMfInb.hIHeHD = false; } else {
                        this.AJBHGO.hMfInb.hIHeHD = true;
                        LLFKph.LKkafb(JLJeih + 'move', 1, false, 0, true);
                    };
                    if (this.acaemD != '') {
                        var mnfIoP = dCibpa(this.acaemD.substring(1));
                        if (mnfIoP < 21) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
                        LLFKph.LKkafb(JLJeih + 'kill', 1, false, 0, true);
                    }
                } else { this.njcLkJ(); }
            };
        };
        hJEkmd.prototype.BAAkAa = function() {
            if (!this.OFPgOl) { return; };
            if (this.AJBHGO) {
                this.mHolDN = this.mHolDN + BLAZE.afEDBA.ddnjdC;
                if (this.mHolDN < this.DnGDMp) {
                    this.IEeIMH = (this.mHolDN / this.DnGDMp) * this.bJiMEP;
                    var pehbDg = AEOgJp.kDMBPo(this.aKbblp, this.IEeIMH / this.bJiMEP);
                    AEOgJp.pjMFnl(pehbDg, this.jemKaO);
                    if (this.dNNHfe) {
                        var NbgEcL = Math.abs(this.IEeIMH - this.GfihNB);
                        NbgEcL = bjAFpk - (bjAFpk * NbgEcL * NbgEcL * this.McLJef);
                        pehbDg[1] = pehbDg[1] - NbgEcL;
                    };
                    this.AJBHGO.ooLIDD = pehbDg;
                    this.JPfdKP.jeEAJP();
                    return;
                };
                this.AJBHGO.ooLIDD = this.HPiFCa;
            };
            this.njcLkJ();
            this.JPfdKP.jeEAJP();
        };
        hJEkmd.prototype.GCgkeK = function(KcMelf) {
            var hKPAKA = KcMelf.target;
            if (KcMelf.type == 'touchend') {
                if (KcMelf.changedTouches.length < 1) { return; };
                var nJogbk = KcMelf.changedTouches[0];
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                hKPAKA = document.elementFromPoint(nJogbk.clientX, nJogbk.clientY);
            } else if (KcMelf.type == 'touchstart') {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
            };
            if (!hKPAKA) { return; };
            if (!hKPAKA.parentNode) { return; };
            if (!hKPAKA.parentNode.eoIjGL) { return; };
            hKPAKA.parentNode.eoIjGL.ppCDLa(KcMelf.type, hKPAKA.kCmaeC);
        };
        hJEkmd.prototype.ppCDLa = function(fogfBH, kCmaeC) {
            if (this.nlemFe) { this.GilbBF(); return; };
            if (!this.aiIcIi || !this.aGEjAM.cOPbiG || this.OFPgOl || this.fjdCgI < 1) { return; };
            kCmaeC = dCibpa(kCmaeC);
            var iBamkN, JLJeih, cJcdCM, cIhEIM;
            var MlnmKA = kCmaeC % 8;
            var HloEke = (kCmaeC - MlnmKA) / 8;
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            kCmaeC = HloEke * 8 + MlnmKA;
            var aCHjkF = 0;
            for (var KgDnNJ in this.FIeFfN) { if (this.FIeFfN[KgDnNJ][0] == kCmaeC) { aCHjkF = dCibpa(KgDnNJ.substring(1)); break; } };
            this.iMEbme(this.fjdCgI);
            if (this.fHNDkc == 0) {
                if (fogfBH == 'mousedown' || fogfBH == 'touchstart') {
                    if (aCHjkF > 0) {
                        if (this.fjdCgI == 1) {
                            if (aCHjkF > 20) { return; };
                            JLJeih = this.NdeLeg;
                        } else if (this.fjdCgI == 2) {
                            if (aCHjkF < 21) { return; };
                            JLJeih = this.GhMInF;
                        } else { return; };
                        LLFKph.LKkafb(JLJeih + 'click', 1, false, 0, true);
                        this.BgCLbl = [];
                        this.fHNDkc = aCHjkF;
                        this.nKdkCL = kCmaeC;
                        this.aPiOCB(kCmaeC);
                        this.kOcLKF = this.BiipIN(this.fHNDkc);
                        if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); }
                    };
                }
            } else {
                if (fogfBH == 'mousedown' || fogfBH == 'touchstart') {
                    if (!this.gAOEgM) {
                        if (this.fHNDkc == aCHjkF || this.nKdkCL == kCmaeC) {} else {
                            if (aCHjkF > 0) {
                                if (this.fjdCgI == 1) {
                                    if (aCHjkF > 20) { return; };
                                    JLJeih = this.NdeLeg;
                                } else if (this.fjdCgI == 2) {
                                    if (aCHjkF < 21) { return; };
                                    JLJeih = this.GhMInF;
                                } else { return; };
                                this.BgCLbl = [];
                                this.fHNDkc = aCHjkF;
                                this.nKdkCL = kCmaeC;
                                this.aPiOCB(kCmaeC);
                                this.kOcLKF = this.BiipIN(this.fHNDkc);
                                if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); };
                                LLFKph.LKkafb(JLJeih + 'click', 1, false, 0, true);
                            }
                        };
                    }
                } else if (fogfBH == 'mouseup' || fogfBH == 'touchend') {
                    if (this.kOcLKF) {
                        var hnmECj = '_' + kCmaeC;
                        if (this.kOcLKF.hasOwnProperty(hnmECj)) {
                            this.BgCLbl.push(kCmaeC);
                            this.hEPkfB([]);
                            var LNfmCG = [
                                [this.fHNDkc, kCmaeC]
                            ];
                            if (this.fHNDkc == 16 || this.fHNDkc == 36) { cIhEIM = this.hkLMbI.length; for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var CFKIBC = this.hkLMbI[cJcdCM]; if (kCmaeC == CFKIBC[1]) { LNfmCG.push([CFKIBC[0], CFKIBC[2], true]); } }; };
                            this.ckIaEI(LNfmCG);
                            var aDlnMk = this.kOcLKF[hnmECj];
                            if (aDlnMk > 0) { aDlnMk = '_' + aDlnMk; if (this.FIeFfN[aDlnMk]) { delete this.FIeFfN[aDlnMk]; } };
                            this.FIeFfN['_' + this.fHNDkc][0] = kCmaeC;
                            this.kOcLKF = null;
                            this.bhlHJO = null;
                            this.ejAHOl = {};
                            this.fjdCgI = 0;
                            this.PMiHiP();
                            this.JKdCgI.pPEGkJ({ c: 'move', v: this.fHNDkc + ':' + this.BgCLbl.join(':') });
                            this.BgCLbl = [];
                            this.JKdCgI.BNkojA();
                        }
                    };
                }
            };
        };
        hJEkmd.prototype.BiipIN = function(aCHjkF) { if (this.bhlHJO) { var KgDnNJ = '_' + aCHjkF; if (this.bhlHJO[KgDnNJ]) { return this.bhlHJO[KgDnNJ]; } }; return { aeDnaK: [] }; };
        hJEkmd.prototype.iMEbme = function(kEJgnC) {
            if (this.bhlHJO) { return; };
            this.bhlHJO = {};
            this.ejAHOl = {};
            var cJcdCM, cIhEIM, KgDnNJ, aCHjkF;
            var iCjDFG = [];
            var pnPAjA = [];
            var cPJhlM = {};
            for (KgDnNJ in this.FIeFfN) {
                aCHjkF = dCibpa(KgDnNJ.substring(1));
                cPJhlM['_' + this.FIeFfN[KgDnNJ][0]] = aCHjkF;
                if (kEJgnC == 1) { if (aCHjkF < 21) { iCjDFG.push(aCHjkF); continue; } } else { if (aCHjkF > 20) { iCjDFG.push(aCHjkF); continue; } };
                pnPAjA.push(aCHjkF);
            };
            cIhEIM = pnPAjA.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                aCHjkF = pnPAjA[cJcdCM];
                KgDnNJ = '_' + aCHjkF;
                this.MPMEim(aCHjkF, cPJhlM, true);
            };
            cIhEIM = iCjDFG.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                aCHjkF = iCjDFG[cJcdCM];
                KgDnNJ = '_' + aCHjkF;
                this.bhlHJO[KgDnNJ] = this.MPMEim(aCHjkF, cPJhlM, false);
            };
            cIhEIM = pnPAjA.length;
            var bgciik = Object.keys(this.bhlHJO);
            var gNcbKl = bgciik.length;
            for (var flOAnn = 0; flOAnn < gNcbKl; flOAnn++) {
                KgDnNJ = bgciik[flOAnn];
                aCHjkF = dCibpa(KgDnNJ.substring(1));
                var OPedaH = this.bhlHJO[KgDnNJ];
                var BoNaIL = { aeDnaK: [] };
                for (var FKfcOk in OPedaH) {
                    var cFakob = dCibpa(FKfcOk.substring(1));
                    if (FKfcOk[0] == '_') {
                        var koMBFo = 0;
                        var JLhoDi = this.aADKjE(cPJhlM, aCHjkF);
                        if (JLhoDi.hasOwnProperty(FKfcOk)) { koMBFo = JLhoDi[FKfcOk]; };
                        JLhoDi[FKfcOk] = aCHjkF;
                        var NcnnOP = false;
                        for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { if (koMBFo != pnPAjA[cJcdCM]) { var gceHgN = this.MPMEim(pnPAjA[cJcdCM], JLhoDi, false); if (gceHgN.NcnnOP) { NcnnOP = true; break; } }; };
                        if (NcnnOP) { continue; };
                        BoNaIL[FKfcOk] = OPedaH[FKfcOk];
                        BoNaIL.aeDnaK.push(cFakob);
                    }
                };
                if (BoNaIL.aeDnaK.length > 0) { this.bhlHJO[KgDnNJ] = BoNaIL; } else { delete this.bhlHJO[KgDnNJ]; }
            };
        };
        hJEkmd.prototype.MPMEim = function(aCHjkF, cPJhlM, NmfdhM) {
            var cJcdCM, cIhEIM, fKjeoh, flOAnn, CFKIBC, FKfcOk, cFakob, KgDnNJ, GGacAl, NbgEcL;
            var ofMhiD = this.oECmEe[1];
            var gceHgN = { aeDnaK: [], NcnnOP: false };
            KgDnNJ = '_' + aCHjkF;
            if (!this.FIeFfN[KgDnNJ]) { return gceHgN; };
            var PFInhD = this.FIeFfN[KgDnNJ][0];
            var ljmKpp = this.cDHGgP(PFInhD);
            var CPKMOI = false;
            var jMDjil = aCHjkF < 21;
            var AdlFOn, jCHLkG;
            var PbfHJM = aCHjkF % 20;
            if (this.FIeFfN[KgDnNJ][1] > 0) { PbfHJM = 15; };
            var FOgJam = null;
            var haJmOP = null;
            if (PbfHJM == 16) {
                CPKMOI = true;
                FOgJam = this.bpmknm._6;
            } else if (PbfHJM == 15) { FOgJam = this.bpmknm._5; } else if (PbfHJM >= 13) { FOgJam = this.bpmknm._4; } else if (PbfHJM >= 11) { FOgJam = this.bpmknm._3; } else if (PbfHJM >= 9) { FOgJam = this.bpmknm._2; } else {
                if (jMDjil) {
                    if (ljmKpp[0] == 1) { FOgJam = this.bpmknm._1WF; } else { FOgJam = this.bpmknm._1W; };
                    haJmOP = this.bpmknm._1WC;
                } else {
                    if (ljmKpp[0] == 6) { FOgJam = this.bpmknm._1BF; } else { FOgJam = this.bpmknm._1B; };
                    haJmOP = this.bpmknm._1BC;
                }
            };
            if (CPKMOI && !NmfdhM) {
                cIhEIM = this.hkLMbI.length;
                for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    CFKIBC = this.hkLMbI[cJcdCM];
                    cFakob = CFKIBC[1];
                    gceHgN['_' + cFakob] = CFKIBC[0];
                    gceHgN.aeDnaK.push(cFakob);
                }
            };
            var kNMNiB = FOgJam.length;
            for (flOAnn = 0; flOAnn < kNMNiB; flOAnn++) {
                CFKIBC = FOgJam[flOAnn];
                cIhEIM = CFKIBC.length;
                for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    GGacAl = AEOgJp.olNCjJ(ljmKpp, CFKIBC[cJcdCM]);
                    if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                    if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                    cFakob = GGacAl[1] * 8 + GGacAl[0];
                    FKfcOk = '_' + cFakob;
                    if (CPKMOI && !NmfdhM) { if (this.ejAHOl[FKfcOk]) { break; } };
                    if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                        if (NmfdhM && !haJmOP) { this.ejAHOl[FKfcOk] = true; };
                        gceHgN[FKfcOk] = 0;
                        gceHgN.aeDnaK.push(cFakob);
                    } else if (haJmOP) { break; } else {
                        fKjeoh = cPJhlM[FKfcOk];
                        if (this.FIeFfN['_' + fKjeoh]) {
                            if (jMDjil && fKjeoh < 21) {} else if (!jMDjil && fKjeoh > 20) {} else {
                                if (NmfdhM && !haJmOP) { this.ejAHOl[FKfcOk] = true; };
                                gceHgN[FKfcOk] = fKjeoh;
                                gceHgN.aeDnaK.push(cFakob);
                                if (fKjeoh == 16 || fKjeoh == 36) { gceHgN.NcnnOP = true; }
                            };
                            break;
                        }
                    };
                }
            };
            if (haJmOP) {
                kNMNiB = haJmOP.length;
                for (flOAnn = 0; flOAnn < kNMNiB; flOAnn++) {
                    CFKIBC = haJmOP[flOAnn];
                    cIhEIM = CFKIBC.length;
                    for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                        GGacAl = AEOgJp.olNCjJ(ljmKpp, CFKIBC[cJcdCM]);
                        if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                        if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                        cFakob = GGacAl[1] * 8 + GGacAl[0];
                        FKfcOk = '_' + cFakob;
                        if (!cPJhlM.hasOwnProperty(FKfcOk)) { if (NmfdhM) { this.ejAHOl[FKfcOk] = true; }; break; } else {
                            fKjeoh = cPJhlM[FKfcOk];
                            if (this.FIeFfN['_' + fKjeoh]) {
                                if (jMDjil && fKjeoh < 21) {} else if (!jMDjil && fKjeoh > 20) {} else {
                                    if (NmfdhM) { this.ejAHOl[FKfcOk] = true; };
                                    gceHgN[FKfcOk] = fKjeoh;
                                    gceHgN.aeDnaK.push(cFakob);
                                    if (fKjeoh == 16 || fKjeoh == 36) { gceHgN.NcnnOP = true; }
                                };
                                break;
                            }
                        };
                    }
                };
                FOgJam = [
                    [0, 1],
                    [0, -1]
                ];
                kNMNiB = FOgJam.length;
                for (cJcdCM = 0; cJcdCM < kNMNiB; cJcdCM++) {
                    GGacAl = AEOgJp.olNCjJ(ljmKpp, FOgJam[cJcdCM]);
                    if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                    if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                    cFakob = GGacAl[1] * 8 + GGacAl[0];
                    FKfcOk = '_' + cFakob;
                    if (cPJhlM.hasOwnProperty(FKfcOk)) {
                        fKjeoh = cPJhlM[FKfcOk];
                        if (this.OdghkO['_' + fKjeoh]) {
                            if (jMDjil) { GGacAl[0] = GGacAl[0] + 1; } else { GGacAl[0] = GGacAl[0] - 1; };
                            cFakob = GGacAl[1] * 8 + GGacAl[0];
                            FKfcOk = '_' + cFakob;
                            if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                                gceHgN[FKfcOk] = 999;
                                gceHgN.aeDnaK.push(cFakob);
                            }
                        };
                    }
                };
            };
            return gceHgN;
        };
        hJEkmd.prototype.aADKjE = function(cPJhlM, oMaAhg) { var JLhoDi = {}; for (var kCmaeC in cPJhlM) { var aCHjkF = cPJhlM[kCmaeC]; if (oMaAhg != aCHjkF) { JLhoDi[kCmaeC] = aCHjkF; } }; return JLhoDi; };
        return function() { return new aGEjAM(new hJEkmd(arguments)) };
    })();
    BLAZE.EGhJiA = EGhJiA;
    var NjLaCP = (function() {
        var aaPJke = BLAZE.GetENV('PROJECT_CONTENT_URL');
        var BgGFbP = [1400, 1000];
        var keDPed = [2, 3];
        var NcFLDH = 116;
        var fPkDGh = 36;
        var LePbiJ = [94, 94];
        var Bnfnhl = 12;
        var NaOHPK = 0.15;
        var hGKBio = 0.3;
        var bjAFpk = 120;
        var aGEjAM = function(GnalKe) {
            var ijmEGj = GnalKe;
            GnalKe.aGEjAM = this;
            this.bIGpib = 0;
            this.cOPbiG = false;
            this.PAFPjb = false;
            this.COhpno = function(oNAeLc, emFjKC, gBdoHa) { return ijmEGj.COhpno(oNAeLc, emFjKC, gBdoHa); };
            this.ajgNIF = function() { ijmEGj.ajgNIF(); };
            this.jNfMiL = function(ajJgBK) { ijmEGj.jNfMiL(ajJgBK); };
            this.NBOOaE = function() { ijmEGj.NBOOaE(); };
            this.BCAKgm = function() { ijmEGj.BCAKgm(); };
            this.HjKaLb = function() { ijmEGj.HjKaLb(); };
            this.fpCIhi = function(INfAAc) { ijmEGj.fpCIhi(INfAAc); };
            this.dpneGd = function(JkgjnL) { ijmEGj.dpneGd(JkgjnL); };
            this.ICBiai = function(bekBpl) { ijmEGj.ICBiai(bekBpl); };
            this.OcDfbM = function(GhNgbO) { ijmEGj.OcDfbM(GhNgbO); };
        };
        var hJEkmd = function(MCaldm) { this.OLBcNb(MCaldm); };
        hJEkmd.prototype.OLBcNb = function(MCaldm) {
            if (MCaldm.length < 2) { $error(20819591); return; };
            if (this.JKdCgI) { $error(20819592); return; };
            if (!epCcje(MCaldm[0])) { $error(20819593); return; };
            if (MCaldm[1]) { MeHcPi = 1; } else { MeHcPi = 0; };
            this.aGEjAM = null;
            this.mKjdCO = BLAZE.DPEkhd.amlcmM();
            this.aiIcIi = false;
            this.IOnEGD();
            this.JKdCgI = MCaldm[0];
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
            this.JPfdKP = new BLAZE.aajFEA('ChessRenderer', BgGFbP[1], BgGFbP[1], 1, MeHcPi);
            this.JPfdKP.jICMmC = true;
            this.JPfdKP.iKDDhb = false;
            this.JPfdKP.gkbHnn = false;
            this.JPfdKP.hKPAKA.cncHOL = true;
            this.oOJDaI = BLAZE.DPEkhd.cFgHGM('element', 'game.checkers_table');
            if (!this.oOJDaI) { $error(63950928); return; };
            dLeLMm.dHBnji(this.oOJDaI);
            this.oOJDaI.IgCMNE = true;
            var BMnhpo = this.oOJDaI.GigegA;
            var aeDnaK = BMnhpo.table_sectors;
            var cJcdCM = 0;
            for (var PIdIFL = 0; PIdIFL < 8; PIdIFL++) {
                var anNKlf = document.createElement('div');
                anNKlf.className = 'ChessTableRow';
                anNKlf.eoIjGL = this;
                aeDnaK.appendChild(anNKlf);
                for (var iFnjBg = 0; iFnjBg < 8; iFnjBg++) {
                    var PfIHKb = BLAZE.DPEkhd.LJNFJi('game.checkers_sector', false);
                    PfIHKb.kCmaeC = cJcdCM;
                    anNKlf.appendChild(PfIHKb);
                    BMnhpo['s_' + cJcdCM] = PfIHKb;
                    BMnhpo['a_' + cJcdCM] = PfIHKb;
                    cJcdCM++;
                }
            };
            aeDnaK.addEventListener('touchend', this.GCgkeK, true);
            aeDnaK.addEventListener('touchstart', this.GCgkeK, true);
            aeDnaK.addEventListener('mouseup', this.GCgkeK, true);
            aeDnaK.addEventListener('mousedown', this.GCgkeK, true);
            this.OOJBGg = BLAZE.DPEkhd.cFgHGM('element', 'game.checkers_select');
            this.nfMJfe = BLAZE.DPEkhd.cFgHGM('element', 'game.checkers_flash');
            var mdKOEp = this;
        };
        hJEkmd.prototype.COhpno = function(oNAeLc, emFjKC, gBdoHa) {
            if (!this.JKdCgI) { $warn(2290681); return false; };
            if (this.aiIcIi) { $warn(2290682); return false; };
            if (!oNAeLc) { $warn(2290683); return false; };
            if (!emFjKC) { $warn(2290684); return false; };
            var NHDmDG = 0;
            if (gBdoHa) { NHDmDG = 1; };
            if (MeHcPi != NHDmDG) {
                MeHcPi = NHDmDG;
                this.JPfdKP.NOjeil();
                this.JPfdKP.nbIBPk();
                this.JPfdKP = new BLAZE.aajFEA('ChessRenderer', BgGFbP[1], BgGFbP[1], 1, MeHcPi);
                this.JPfdKP.jICMmC = true;
                this.JPfdKP.iKDDhb = false;
                this.JPfdKP.gkbHnn = false;
                this.JPfdKP.hKPAKA.cncHOL = true;
            };
            this.aGEjAM.bIGpib = 0;
            this.IOnEGD();
            if (emFjKC.length != 11) { $warn(64223638); return false; };
            emFjKC[2] = dCibpa(emFjKC[2]);
            emFjKC[3] = dCibpa(emFjKC[3]);
            emFjKC[4] = dCibpa(emFjKC[4]);
            emFjKC[5] = dCibpa(emFjKC[5]);
            emFjKC[6] = dCibpa(emFjKC[6]);
            emFjKC[7] = dCibpa(emFjKC[7]);
            this.oECmEe = emFjKC;
            this.AbOpkd = emFjKC[5] == 1;
            this.kmJAAO = oNAeLc;
            var GigegA = this.kmJAAO.GigegA;
            this.dfOJLM = oNAeLc.parentNode;
            if (!this.dfOJLM) { $error(95882103); return; };
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.hLngmL = GigegA.GameScoreboard;
            this.lpLlFE = GigegA.GameArea;
            this.DLchLC = GigegA.GameFullZone;
            this.lpPabJ = GigegA.GameTable;
            this.lpPabJ.appendChild(this.oOJDaI);
            this.JPfdKP.IhnhPd(this.lpPabJ);
            this.JKdCgI.aaipCF(BgGFbP, false);
            this.hGcmiD(emFjKC[7], emFjKC[8]);
            this.aiIcIi = true;
            return true;
        };
        hJEkmd.prototype.ajgNIF = function() {
            if (!this.JKdCgI) { $warn(59029918); return; };
            this.Fgbpjh(1, '');
            this.Fgbpjh(2, '');
            this.hEPkfB([]);
            this.PMiHiP();
            this.IOnEGD();
            this.aiIcIi = false;
            if (this.OOJBGg) { if (this.OOJBGg.parentNode) { this.OOJBGg.parentNode.removeChild(this.OOJBGg); } };
            if (this.nfMJfe) { if (this.nfMJfe.parentNode) { this.nfMJfe.parentNode.removeChild(this.nfMJfe); } };
            if (this.oOJDaI) { if (this.oOJDaI.parentNode) { this.oOJDaI.parentNode.removeChild(this.oOJDaI); } };
            if (this.JPfdKP) {
                this.JPfdKP.nbIBPk();
                this.JPfdKP.aMiNKa();
            };
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
        };
        hJEkmd.prototype.HjKaLb = function() {
            this.ajgNIF();
            this.JKdCgI = null;
            this.OOJBGg = null;
            this.nfMJfe = null;
            this.oOJDaI = null;
            this.JPfdKP = null;
        };
        hJEkmd.prototype.IOnEGD = function() {
            this.nlemFe = null;
            this.jHPcHF = false;
            this.jDPhKk = 0;
            this.GBnioj = '';
            this.oECmEe = null;
            this.AbOpkd = false;
            this.IfHNmH = { _1: [], _2: [] };
            this.gaIpJE = [];
            this.ADeOCF = [];
            this.cpHPfC = 1.0;
            this.hgbGol = null;
            this.fjdCgI = 0;
            this.BcKPJA = 0;
            this.gAOEgM = false;
            this.fHNDkc = 0;
            this.nKdkCL = 0;
            this.kOcLKF = null;
            this.BgCLbl = [];
            this.jDChHC = -1;
            this.NdeLeg = '';
            this.GhMInF = '';
            this.ceNmop = null;
            this.eGADpE = null;
            this.FIeFfN = {};
            this.JAcmEK = {};
            this.bhlHJO = null;
            this.nAilaH = '';
            this.nloDdm = null;
            this.OFPgOl = false;
            this.DnGDMp = 0;
            this.BIAnlc = -1;
            this.gIklBa = [];
            this.AJBHGO = null;
            this.acaemD = '';
            this.cOhCGk = -1;
            this.jemKaO = null;
            this.HPiFCa = null;
            this.bJiMEP = 0;
            this.GfihNB = 0;
            this.mHolDN = 0;
            this.IEeIMH = 0;
            this.aKbblp = null;
            this.McLJef = 0;
            this.dNNHfe = false;
        };
        hJEkmd.prototype.dpneGd = function(JkgjnL) {
            if (!this.aiIcIi) { return; };
            if (this.oOJDaI) {
                var gNcbKl = this.oOJDaI.GigegA;
                var hKPAKA = gNcbKl.BHLoEL;
                if (!hKPAKA) {
                    hKPAKA = gNcbKl.table_super_game;
                    if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                    this.lpPabJ.appendChild(hKPAKA);
                    gNcbKl.BHLoEL = hKPAKA;
                };
                var gNcbKl = this.oOJDaI.GigegA;
                gNcbKl.table_super_game_zp.innerHTML = JkgjnL + ' ZP';
                hKPAKA.classList.add('AnimSuperGame');
            }
        };
        hJEkmd.prototype.OcDfbM = function(bJhmlj) {
            if (!this.aiIcIi) { return; };
            var EjJIlL, iBamkN, GhNgbO;
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.PacccC = dLeLMm.OnKbCc(this.BcoPPH);
            bJhmlj[0] -= bJhmlj[0] % 8;
            bJhmlj[1] -= bJhmlj[1] % 8;
            var hEdBhi = bJhmlj[0] + 'px';
            var EjbkCN = bJhmlj[1] + 'px';
            var oKcDNc = '';
            var BkKhgB = '';
            var pMAMeL = '';
            var eDGEAM = bJhmlj[0] >= bJhmlj[1];
            if (eDGEAM) {
                oKcDNc = bJhmlj[1] + 'px';
                BkKhgB = '0px';
                pMAMeL = Math.round((bJhmlj[0] - bJhmlj[1]) * 0.5) + 'px';
                this.cpHPfC = bJhmlj[0] / BgGFbP[0];
            } else {
                oKcDNc = bJhmlj[0] + 'px';
                BkKhgB = Math.round((bJhmlj[1] - bJhmlj[0]) * 0.5) + 'px';
                pMAMeL = '0px';
                this.cpHPfC = bJhmlj[1] / BgGFbP[0];
            };
            var s, l;
            if (this.oOJDaI) {
                s = this.oOJDaI.style;
                s.width = s.height = oKcDNc;
                s.top = BkKhgB;
                s.left = pMAMeL;
                var BMnhpo = this.oOJDaI.GigegA;
                BMnhpo.table_sectors.style.padding = Math.round(fPkDGh * this.cpHPfC) + 'px';
                var CdjeMc = 0.85;
                var mDAbnB = this.cpHPfC * CdjeMc;
                var haACNG = Math.round((BgGFbP[0] - BgGFbP[1]) * 0.5);
                var eeGObG, HkPNDK, fdDaBe;
                if (eDGEAM) {
                    eeGObG = Math.round(haACNG / CdjeMc) + 'px';
                    HkPNDK = Math.round(BgGFbP[1] / CdjeMc) + 'px';
                } else {
                    eeGObG = Math.round(BgGFbP[1] / CdjeMc) + 'px';
                    HkPNDK = Math.round(haACNG / CdjeMc) + 'px';
                };
                l = BMnhpo.stack_2.classList;
                s = BMnhpo.stack_2.style;
                s.width = eeGObG;
                s.height = HkPNDK;
                if (eDGEAM) {
                    l.remove('StackPortrait');
                    l.add('StackLandscape');
                    s.top = '0px';
                    s.left = '-' + eeGObG;
                    dLeLMm.KEEcac(BMnhpo.stack_2, mDAbnB, mDAbnB);
                } else {
                    l.add('StackPortrait');
                    l.remove('StackLandscape');
                    s.top = '0px';
                    s.left = '0px';
                    dLeLMm.KEEcac(BMnhpo.stack_2, mDAbnB, -mDAbnB);
                };
                l = BMnhpo.stack_1.classList;
                s = BMnhpo.stack_1.style;
                s.width = eeGObG;
                s.height = HkPNDK;
                if (eDGEAM) {
                    l.remove('StackPortrait');
                    l.add('StackLandscape');
                    s.top = '0px';
                    s.bottom = '';
                    s.left = '';
                    s.right = '-' + eeGObG;
                } else {
                    l.add('StackPortrait');
                    l.remove('StackLandscape');
                    s.top = '';
                    s.bottom = '-' + HkPNDK;
                    s.left = '0px';
                    s.right = '';
                };
                dLeLMm.KEEcac(BMnhpo.stack_1, mDAbnB, mDAbnB);
            };
            if (this.JPfdKP) {
                s = this.JPfdKP.hKPAKA.style;
                s.width = s.height = oKcDNc;
                s.top = BkKhgB;
                s.left = pMAMeL;
            };
            this.OepnhE();
        };
        hJEkmd.prototype.jNfMiL = function(ajJgBK) {
            if (!ajJgBK) { return; };
            this.jHPcHF = false;
            this.nlemFe = ajJgBK;
            this.nlemFe.OcMDpE = 0;
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.hgbGol = window.setTimeout(this.bIdfjh, 50, this);
        };
        hJEkmd.prototype.NBOOaE = function() {
            if (!this.nlemFe) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.JKdCgI.aFDeff();
            this.jHPcHF = false;
            this.nlemFe.OcMDpE = 0;
            this.hgbGol = window.setTimeout(this.bIdfjh, 50, this);
        };
        hJEkmd.prototype.GilbBF = function() {
            if (!this.nlemFe) { return; };
            if (this.nlemFe.OcMDpE >= this.nlemFe.bKgEdk.length - 1) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.jHPcHF = true;
            this.JKdCgI.jfBhKJ();
            this.JKdCgI.aFOEfh();
            this.JKdCgI.OEOpEB();
        };
        hJEkmd.prototype.BCAKgm = function() {
            if (!this.nlemFe) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            this.jHPcHF = false;
            this.JKdCgI.BBFIek();
            this.GEGNag();
        };
        hJEkmd.prototype.GEGNag = function() {
            if (!this.nlemFe) { return; };
            if (this.OFPgOl || this.jHPcHF) { return; };
            if (this.hgbGol !== null) { window.clearTimeout(this.hgbGol); };
            var aaONaI = 1500;
            if (this.nlemFe.OcMDpE < 1) { aaONaI = 50; };
            this.hgbGol = window.setTimeout(this.phHGmj, aaONaI, this);
        };
        hJEkmd.prototype.bIdfjh = function(fkiijB) {
            if (!fkiijB.nlemFe || !fkiijB.aiIcIi) { return; };
            fkiijB.pDhCiA();
        };
        hJEkmd.prototype.phHGmj = function(fkiijB) {
            if (!fkiijB.nlemFe || !fkiijB.aiIcIi) { return; };
            if (this.OFPgOl || this.jHPcHF) { return; };
            var OcMDpE = fkiijB.nlemFe.OcMDpE;
            var bKgEdk = fkiijB.nlemFe.bKgEdk;
            if (OcMDpE < bKgEdk.length) {
                var PfIHKb = bKgEdk[OcMDpE];
                OcMDpE = OcMDpE + 1;
                fkiijB.nlemFe.OcMDpE = OcMDpE;
                fkiijB.fpCIhi(PfIHKb);
            } else { fkiijB.JKdCgI.BBFIek(); }
        };
        hJEkmd.prototype.pDhCiA = function() {
            if (!this.aiIcIi) { return; };
            var iBamkN, EjJIlL, ajJgBK, bBOchF;
            var EmNmnC = false;
            if (this.gaIpJE.length > 0) {
                ajJgBK = this.gaIpJE.shift();
                bBOchF = ajJgBK[0];
                if (bBOchF == 'i') {
                    this.GBnioj = ajJgBK[1];
                    this.JKdCgI.cBIfjo();
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.OFPgOl = false;
                    this.gIklBa = [];
                    EmNmnC = true;
                    this.DeKAaj();
                } else if (bBOchF == 's') {
                    iBamkN = ajJgBK[1].split(',');
                    if (iBamkN.length == 2) {
                        EjJIlL = dCibpa(iBamkN[0]);
                        this.ceNmop = BLAZE.DPEkhd.cFgHGM('bitmap', 'checkers_figures_' + EjJIlL);
                        this.NdeLeg = 'chks_' + EjJIlL + '_';
                        EjJIlL = dCibpa(iBamkN[1]);
                        this.eGADpE = BLAZE.DPEkhd.cFgHGM('bitmap', 'checkers_figures_' + EjJIlL);
                        this.GhMInF = 'chks_' + EjJIlL + '_';
                    };
                    if (this.OFPgOl) { this.nAilaH = ajJgBK[2]; } else { this.HBBBbi(ajJgBK[2]); }
                } else if (bBOchF == 'a') {
                    this.BcKPJA = dCibpa(ajJgBK[2]);
                    this.fjdCgI = dCibpa(ajJgBK[1]);
                    this.gAOEgM = false;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.JKdCgI.bLbBKB();
                } else if (bBOchF == 'r') {
                    this.gAOEgM = false;
                    this.fjdCgI = 0;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.JKdCgI.BNkojA();
                } else if (bBOchF == 'p') {
                    var LePFnj = dCibpa(ajJgBK[1]);
                    if ((this.aGEjAM.bIGpib != LePFnj && LePFnj > 0) || !this.aGEjAM.cOPbiG) {
                        this.BcKPJA = dCibpa(ajJgBK[3]);
                        this.haAnCH(dCibpa(ajJgBK[2]), ajJgBK[4].split(':'));
                    }
                } else { $warn('GC ' + bBOchF); }
            };
            if (this.ADeOCF.length > 0 && !EmNmnC) {
                this.JKdCgI.aFDeff();
                var ePoLdm = this.ADeOCF.shift();
                var NlPIck = HiMfgN.dcahnC(MmFnAP() - ePoLdm[0]);
                ajJgBK = ePoLdm[1];
                var cIhEIM = ajJgBK.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    iBamkN = ajJgBK[cJcdCM].split('#');
                    bBOchF = iBamkN[0];
                    if (bBOchF == 'p') { if (iBamkN.length < 4) { this.JKdCgI.HhlhKD(iBamkN[1], IpFeae('computer_player'), iBamkN[3]); } else { this.JKdCgI.HhlhKD(iBamkN[1], iBamkN[2], iBamkN[3]); } } else if (bBOchF == 's') {} else if (bBOchF == 'i') { this.JKdCgI.laipPe(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'h') { this.Fgbpjh(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'j') { this.peaOmi(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'c') { this.JKdCgI.PHafCn(iBamkN[1]); } else if (bBOchF == 't') { this.JKdCgI.abgdOj(dCibpa(iBamkN[1]) + NlPIck, iBamkN[2]); } else if (bBOchF == 'e') { this.JKdCgI.iClGgO(iBamkN[1]); } else if (bBOchF == 'r') { this.JKdCgI.FkCIHc(iBamkN[1], dCibpa(iBamkN[2]) + NlPIck); } else if (bBOchF == 'w') {
                        this.JKdCgI.OEOpEB();
                        if (this.OFPgOl) { this.nloDdm = iBamkN; } else {
                            this.gAOEgM = false;
                            this.fjdCgI = 0;
                            this.fHNDkc = 0;
                            this.nKdkCL = 0;
                            this.hEPkfB([]);
                            this.PMiHiP();
                            this.bhlHJO = null;
                            this.JKdCgI.OEOpEB();
                            this.JKdCgI.JAdFJk(iBamkN[1], iBamkN[2], iBamkN[3], iBamkN[4], iBamkN[5], iBamkN[6]);
                            this.nloDdm = null;
                        }
                    } else if (bBOchF == 'v') { this.JKdCgI.fNCPnN(); var eDLbgB = iBamkN.length; for (var EnibFl = 1; EnibFl < eDLbgB; EnibFl++) { this.JKdCgI.nabEiA(iBamkN[EnibFl]); } } else if (bBOchF == 'l') { this.JKdCgI.nabEiA(iBamkN[1]); } else { $warn('IC ' + bBOchF); }
                };
            };
            if (this.gaIpJE.length > 0 || this.ADeOCF.length > 0) { this.pDhCiA(); } else if (this.nlemFe) { this.GEGNag(); }
        };
        hJEkmd.prototype.fpCIhi = function(INfAAc) {
            if (!this.aiIcIi) { return; };
            if (!INfAAc) { return; };
            if (INfAAc.hasOwnProperty('gcn')) { this.JKdCgI.dFbJkH(); };
            if (INfAAc.hasOwnProperty('cpi')) { this.aGEjAM.bIGpib = dCibpa(INfAAc['cpi']); };
            var gFiOmG = false;
            if (INfAAc.hasOwnProperty('gv')) {
                gFiOmG = true;
                var khFnEl = String(INfAAc.gv).split('|');
                var cIhEIM = khFnEl.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    var IDKdaa = khFnEl[cJcdCM].split('#');
                    var EEkoKP = IDKdaa[0];
                    this.gaIpJE.push(IDKdaa);
                }
            };
            if (INfAAc.hasOwnProperty('gs')) {
                gFiOmG = true;
                this.ADeOCF.push([MmFnAP(), String(INfAAc.gs).split('|')]);
            };
            if (!this.ccehkL && gFiOmG) { this.pDhCiA(); }
        };
        hJEkmd.prototype.ICBiai = function(bekBpl) {
            if (!this.aiIcIi) { return; };
            this.BAAkAa();
        };
        hJEkmd.prototype.hGcmiD = function(MhGMlH, NADDee) {
            MhGMlH = dCibpa(MhGMlH);
            NADDee = dCibpa(NADDee);
            this.jDPhKk = kPpOoh();
            this.JPfdKP.NOjeil();
            this.JAcmEK = {};
            var BMnhpo = this.oOJDaI.GigegA;
            BMnhpo.table_default.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_default_table').src + '")';
            BMnhpo.table_overlay.classList.remove('transition');
            BMnhpo.table_overlay.style.backgroundImage = 'none';
            if (MhGMlH > 0) {
                BMnhpo.table_overlay.style.display = 'block';
                BMnhpo.table_overlay.style.opacity = '0';
                var ePoLdm = 'chb' + MhGMlH;
                BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, this.Lphbgg, this);
            } else { BMnhpo.table_overlay.style.display = 'none'; }
        };
        hJEkmd.prototype.hHGnAN = function() { return (kPpOoh() - this.jDPhKk) < 1000; };
        hJEkmd.prototype.Lphbgg = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki || !NpfeFE) { return; };
            if (!hGbOki.oOJDaI) { return; };
            var hKPAKA = hGbOki.oOJDaI.GigegA.table_overlay;
            hKPAKA.style.backgroundImage = 'url("' + NpfeFE.src + '")';
            if (!hGbOki.hHGnAN()) { hKPAKA.classList.add('transition'); };
            hKPAKA.style.opacity = '1';
        };
        hJEkmd.prototype.HBBBbi = function(hAkImK) {
            this.bhlHJO = null;
            this.nAilaH = '';
            if (!this.aiIcIi) { return; };
            if (!this.oOJDaI) { return; };
            var BMnhpo = this.oOJDaI.GigegA;
            if (this.jDChHC != this.aGEjAM.bIGpib) {
                this.jDChHC = this.aGEjAM.bIGpib;
                if (this.jDChHC == 1 || this.jDChHC == 2) {
                    BMnhpo.table_base.classList.remove('FlipBoard');
                    BMnhpo.table_numbers.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_numbers_' + this.jDChHC).src + '")';
                } else {
                    BMnhpo.table_base.classList.add('FlipBoard');
                    BMnhpo.table_numbers.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'chess_numbers_0').src + '")';
                };
                var iBamkN;
                var aeDnaK = BMnhpo.table_sectors;
                for (var cJcdCM = 0; cJcdCM < 64; cJcdCM++) {
                    var PfIHKb = BMnhpo['s_' + cJcdCM];
                    var kCmaeC = cJcdCM;
                    var MlnmKA = kCmaeC % 8;
                    var HloEke = (kCmaeC - MlnmKA) / 8;
                    if (this.jDChHC == 1) {
                        iBamkN = HloEke;
                        HloEke = MlnmKA;
                        MlnmKA = 7 - iBamkN;
                    } else if (this.jDChHC == 2) {
                        iBamkN = HloEke;
                        HloEke = 7 - MlnmKA;
                        MlnmKA = iBamkN;
                    };
                    kCmaeC = HloEke * 8 + MlnmKA;
                    BMnhpo['a_' + kCmaeC] = PfIHKb;
                }
            };
            this.hEPkfB([]);
            this.PMiHiP();
            this.OFPgOl = false;
            this.gIklBa = [];
            this.FIeFfN = {};
            var khFnEl = hAkImK.split(';');
            var cIhEIM = khFnEl.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var ilcBeA = khFnEl[cJcdCM].split(':'); if (ilcBeA.length == 2) { this.FIeFfN['_' + dCibpa(ilcBeA[0])] = [dCibpa(ilcBeA[1]), 0]; } else if (ilcBeA.length == 3) { this.FIeFfN['_' + dCibpa(ilcBeA[0])] = [dCibpa(ilcBeA[1]), dCibpa(ilcBeA[2])]; } };
            this.OepnhE();
            this.BIOhpL(1);
            this.BIOhpL(2);
        };
        hJEkmd.prototype.DeKAaj = function() {
            this.FIeFfN = {};
            this.OepnhE();
        };
        hJEkmd.prototype.OepnhE = function() {
            if (!this.aiIcIi) { return; };
            if (!this.oOJDaI) { return; };
            if (this.jDChHC < 0) { return; };
            var KgDnNJ;
            for (KgDnNJ in this.FIeFfN) {
                var aCHjkF = dCibpa(KgDnNJ.substring(1));
                var jMDjil = aCHjkF < 21;
                var hKPAKA = this.JAcmEK[KgDnNJ];
                if (!hKPAKA) {
                    if (jMDjil) {
                        hKPAKA = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                        hKPAKA.hMfInb = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                    } else {
                        hKPAKA = new BLAZE.pEMpHD(this.eGADpE, 1, 4, keDPed);
                        hKPAKA.hMfInb = new BLAZE.pEMpHD(this.ceNmop, 1, 4, keDPed);
                    };
                    hKPAKA.lnJkFm(-1, hKPAKA.hMfInb);
                    this.JPfdKP.lnJkFm(-1, hKPAKA);
                    this.JAcmEK[KgDnNJ] = hKPAKA;
                };
                if (!jMDjil) {
                    if (this.FIeFfN[KgDnNJ][1] > 0) {
                        hKPAKA.OmMiOf(3);
                        hKPAKA.hMfInb.OmMiOf(5);
                    } else {
                        hKPAKA.OmMiOf(1);
                        hKPAKA.hMfInb.OmMiOf(4);
                    }
                } else {
                    if (this.FIeFfN[KgDnNJ][1] > 0) {
                        hKPAKA.OmMiOf(2);
                        hKPAKA.hMfInb.OmMiOf(5);
                    } else {
                        hKPAKA.OmMiOf(0);
                        hKPAKA.hMfInb.OmMiOf(4);
                    }
                };
                AEOgJp.MOGook(this.JdBDaN(this.FIeFfN[KgDnNJ][0]), this.JAcmEK[KgDnNJ].ooLIDD);
            };
            var fgEAcn = Object.keys(this.JAcmEK);
            var cIhEIM = fgEAcn.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                KgDnNJ = fgEAcn[cJcdCM];
                if (!this.FIeFfN.hasOwnProperty(KgDnNJ)) {
                    this.JPfdKP.ChmIdn(this.JAcmEK[KgDnNJ]);
                    delete this.JAcmEK[KgDnNJ];
                }
            };
            this.JPfdKP.jeEAJP();
        };
        hJEkmd.prototype.HKloFm = function(ooLIDD) {
            var iBamkN;
            var MlnmKA = Math.round(Math.floor(ooLIDD[0] / NcFLDH));
            var HloEke = Math.round(Math.floor(ooLIDD[1] / NcFLDH));
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            return [MlnmKA, HloEke];
        };
        hJEkmd.prototype.ofFoOg = function(ooLIDD) {
            var iBamkN;
            var MlnmKA = Math.round(Math.floor(ooLIDD[0] / NcFLDH));
            var HloEke = Math.round(Math.floor(ooLIDD[1] / NcFLDH));
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            return Math.round(MlnmKA + (HloEke * 8));
        };
        hJEkmd.prototype.cDHGgP = function(kCmaeC) { var MlnmKA = kCmaeC % 8; var HloEke = (kCmaeC - MlnmKA) / 8; return [MlnmKA, HloEke]; };
        hJEkmd.prototype.JdBDaN = function(kCmaeC) {
            var iBamkN;
            var MlnmKA = kCmaeC % 8;
            var HloEke = (kCmaeC - MlnmKA) / 8;
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            };
            return [(MlnmKA * NcFLDH) + LePbiJ[0], (HloEke * NcFLDH) + LePbiJ[1]];
        };
        hJEkmd.prototype.LBkPnh = function(kCmaeC) { var MlnmKA = kCmaeC % 8; var HloEke = (kCmaeC - MlnmKA) / 8; if (HloEke % 2 == 0) { return MlnmKA % 2 != 0; } else { return MlnmKA % 2 == 0; } };
        hJEkmd.prototype.Fgbpjh = function(mcMdAB, ajJgBK) {
            if (!this.oOJDaI) { return; };
            if (mcMdAB != 1 && mcMdAB != 2) { return; };
            this.IfHNmH['_' + mcMdAB] = [];
            this.peaOmi(mcMdAB, ajJgBK);
        };
        hJEkmd.prototype.peaOmi = function(mcMdAB, ajJgBK) {
            if (!this.oOJDaI) { return; };
            if (mcMdAB != 1 && mcMdAB != 2) { return; };
            var cjIeal = this.IfHNmH['_' + mcMdAB];
            var ilcBeA = ajJgBK.split(':');
            var cIhEIM = ilcBeA.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var iBamkN = ilcBeA[cJcdCM].split('.'); if (iBamkN.length == 2) { cjIeal.push([dCibpa(iBamkN[0]), dCibpa(iBamkN[1])]); } };
            this.BIOhpL(mcMdAB);
        };
        hJEkmd.prototype.BIOhpL = function(mcMdAB) {
            if (!this.oOJDaI) { return; };
            if (!this.ceNmop || !this.eGADpE) { return; };
            var kmJAAO;
            var djCpJK = '';
            if (this.jDChHC == 1) {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else { return; }
            } else if (this.jDChHC == 2) {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else { return; }
            } else {
                if (mcMdAB == 1) {
                    djCpJK = 'url("' + this.eGADpE.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_2'];
                } else if (mcMdAB == 2) {
                    djCpJK = 'url("' + this.ceNmop.src + '")';
                    kmJAAO = this.oOJDaI.GigegA['stack_1'];
                } else { return; }
            };
            var cjIeal = this.IfHNmH['_' + mcMdAB];
            var hKPAKA, cIhEIM = cjIeal.length;
            for (var cJcdCM = 0; cJcdCM < Bnfnhl; cJcdCM++) {
                var hnMkjD = 'S' + cJcdCM;
                var GHcmme = 'E' + cJcdCM;
                if (cJcdCM >= cIhEIM) {
                    hKPAKA = kmJAAO[GHcmme];
                    if (hKPAKA) {
                        if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                        hKPAKA = null;
                        delete kmJAAO[GHcmme];
                    };
                    hKPAKA = kmJAAO[hnMkjD];
                    if (hKPAKA) {
                        if (hKPAKA.parentNode) { hKPAKA.parentNode.removeChild(hKPAKA); };
                        hKPAKA = null;
                        delete kmJAAO[hnMkjD];
                    }
                } else {
                    var iBamkN = cjIeal[cJcdCM];
                    var jMDjil = iBamkN[0] < 21;
                    var CPKMOI = iBamkN[1] > 0;
                    hKPAKA = kmJAAO[hnMkjD];
                    if (!hKPAKA) {
                        hKPAKA = document.createElement('div');
                        kmJAAO[hnMkjD] = hKPAKA;
                        kmJAAO.appendChild(hKPAKA);
                    };
                    hKPAKA.style.backgroundImage = djCpJK;
                    if (CPKMOI) { hKPAKA.className = 'CheckerShadow Frame5'; } else { hKPAKA.className = 'CheckerShadow Frame4'; };
                    hKPAKA = kmJAAO[GHcmme];
                    if (!hKPAKA) {
                        hKPAKA = document.createElement('div');
                        kmJAAO[GHcmme] = hKPAKA;
                        kmJAAO[hnMkjD].appendChild(hKPAKA);
                    };
                    hKPAKA.style.backgroundImage = djCpJK;
                    if (jMDjil) { if (CPKMOI) { hKPAKA.className = 'CheckerFigure Frame2'; } else { hKPAKA.className = 'CheckerFigure Frame0'; } } else { if (CPKMOI) { hKPAKA.className = 'CheckerFigure Frame3'; } else { hKPAKA.className = 'CheckerFigure Frame1'; } };
                }
            };
        };
        hJEkmd.prototype.aPiOCB = function(kCmaeC) {
            if (!this.oOJDaI || !this.OOJBGg) { return; };
            this.PMiHiP();
            if (this.OOJBGg.parentNode) { this.OOJBGg.parentNode.removeChild(this.OOJBGg); };
            this.OOJBGg.classList.remove('Transition');
            this.OOJBGg.style.opacity = 1;
            var BMnhpo = this.oOJDaI.GigegA;
            var JdinEc = 'a_' + kCmaeC;
            if (!BMnhpo[JdinEc]) { return; };
            BMnhpo[JdinEc].appendChild(this.OOJBGg);
        };
        hJEkmd.prototype.PMiHiP = function() {
            if (this.OOJBGg) {
                this.OOJBGg.classList.add('Transition');
                this.OOJBGg.style.opacity = 0;
            }
        };
        hJEkmd.prototype.PeMPlE = function(kCmaeC) {
            if (!this.oOJDaI || !this.nfMJfe) { return; };
            if (this.nfMJfe.parentNode) { this.nfMJfe.parentNode.removeChild(this.nfMJfe); };
            var BMnhpo = this.oOJDaI.GigegA;
            var JdinEc = 'a_' + kCmaeC;
            if (!BMnhpo[JdinEc]) { return; };
            BMnhpo[JdinEc].appendChild(this.nfMJfe);
            this.nfMJfe.style.display = 'none';
            this.nfMJfe.classList.remove('Animation');
            this.nfMJfe.style.display = '';
            this.nfMJfe.classList.add('Animation');
        };
        hJEkmd.prototype.hEPkfB = function(aeDnaK) {
            if (!this.oOJDaI) { return; };
            var BMnhpo = this.oOJDaI.GigegA;
            var miChPH = {};
            var cJcdCM, cIhEIM = aeDnaK.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { miChPH['_' + aeDnaK[cJcdCM]] = true; };
            for (cJcdCM = 0; cJcdCM < 64; cJcdCM++) {
                var PfIHKb = BMnhpo['a_' + cJcdCM];
                if (PfIHKb) {
                    if (miChPH['_' + cJcdCM]) { if (this.LBkPnh(cJcdCM)) { PfIHKb.classList.add('CH_White'); } else { PfIHKb.classList.add('CH_Black'); } } else {
                        PfIHKb.classList.remove('CH_Black');
                        PfIHKb.classList.remove('CH_White');
                    }
                };
            }
        };
        hJEkmd.prototype.haAnCH = function(aCHjkF, DJMeFO) {
            if (!DJMeFO) { return; };
            if (!this.aiIcIi) { return; };
            var gceHgN = [];
            var cIhEIM = DJMeFO.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { gceHgN.push([aCHjkF, dCibpa(DJMeFO[cJcdCM])]); };
            this.ckIaEI(gceHgN);
        };
        hJEkmd.prototype.ckIaEI = function(gceHgN) {
            if (!gceHgN) { return; };
            if (!this.aiIcIi) { return; };
            if (this.OFPgOl) {
                var cIhEIM = this.gIklBa.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var hegNOA = this.gIklBa[cJcdCM]; var KgDnNJ = '_' + hegNOA[0]; var fNbdEN = dCibpa(hegNOA[1]) % 64; if (this.JAcmEK[KgDnNJ]) { this.JAcmEK[KgDnNJ].ooLIDD = this.JdBDaN(fNbdEN); } };
                this.JPfdKP.jeEAJP();
            };
            this.OFPgOl = true;
            this.gIklBa = gceHgN;
            this.njcLkJ();
        };
        hJEkmd.prototype.njcLkJ = function() {
            if (!this.aiIcIi || !this.OFPgOl) { return; };
            var JLJeih;
            if (this.acaemD != '') {
                if (this.JAcmEK[this.acaemD]) {
                    this.JPfdKP.ChmIdn(this.JAcmEK[this.acaemD]);
                    delete this.JAcmEK[this.acaemD];
                };
                this.acaemD = '';
            };
            if (this.BIAnlc > 20) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
            if (this.BIAnlc > 0) { if (this.dNNHfe) { LLFKph.LKkafb(JLJeih + 'hit', 1, false, 0, true); } };
            if (this.gIklBa.length < 1) {
                if (this.BIAnlc >= 0 && this.AJBHGO && !this.gAOEgM) {
                    var mceNlo = '_' + this.BIAnlc;
                    if (this.FIeFfN[mceNlo]) {
                        if (this.FIeFfN[mceNlo][1] == 0) {
                            var Hklaap = this.cDHGgP(this.cOhCGk);
                            var lDHPFJ = -1;
                            if (this.BIAnlc < 21) { if (Hklaap[0] == 7) { lDHPFJ = 2; } } else { if (Hklaap[0] == 0) { lDHPFJ = 3; } };
                            if (lDHPFJ >= 0) {
                                LLFKph.LKkafb(JLJeih + 'crowned', 1, false, 0, true);
                                this.AJBHGO.OmMiOf(lDHPFJ);
                            }
                        };
                    }
                };
                if (this.AJBHGO) {
                    this.AJBHGO.hMfInb.hIHeHD = true;
                    this.AJBHGO = null;
                };
                this.BIAnlc = -1;
                this.OFPgOl = false;
                if (this.nAilaH != '') { this.HBBBbi(this.nAilaH); } else { this.JPfdKP.jeEAJP(); };
                if (this.gAOEgM) { if (this.kOcLKF) { if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); } }; };
                if (this.nloDdm) {
                    this.gAOEgM = false;
                    this.fjdCgI = 0;
                    this.fHNDkc = 0;
                    this.nKdkCL = 0;
                    this.hEPkfB([]);
                    this.PMiHiP();
                    this.bhlHJO = null;
                    this.JKdCgI.OEOpEB();
                    this.JKdCgI.JAdFJk(this.nloDdm[1], this.nloDdm[2], this.nloDdm[3], this.nloDdm[4], this.nloDdm[5], this.nloDdm[6]);
                    this.nloDdm = null;
                };
                if (this.nlemFe) { this.GEGNag(); }
            } else {
                var hegNOA = this.gIklBa.shift();
                var KgDnNJ = '_' + hegNOA[0];
                var fNbdEN = dCibpa(hegNOA[1]) % 64;
                if (this.JAcmEK[KgDnNJ]) {
                    if (!this.gAOEgM) { this.PeMPlE(fNbdEN); };
                    this.OFPgOl = true;
                    this.BIAnlc = hegNOA[0];
                    this.acaemD = '';
                    this.AJBHGO = this.JAcmEK[KgDnNJ];
                    this.cOhCGk = fNbdEN;
                    this.HPiFCa = this.JdBDaN(fNbdEN);
                    this.jemKaO = AEOgJp.clhoEK(this.AJBHGO.ooLIDD);
                    this.aKbblp = AEOgJp.GajdDk(this.HPiFCa, this.jemKaO);
                    this.bJiMEP = AEOgJp.FkDjcj(this.aKbblp);
                    this.GfihNB = this.bJiMEP * 0.5;
                    this.McLJef = 1 / this.GfihNB / this.GfihNB;
                    this.mHolDN = 0;
                    this.IEeIMH = 0;
                    this.dNNHfe = this.bJiMEP / NcFLDH > 1.9;
                    if (this.dNNHfe) { this.DnGDMp = hGKBio; } else { this.DnGDMp = NaOHPK; };
                    if (this.dNNHfe) {
                        var cJcdCM, FKfcOk;
                        var cPJhlM = {};
                        for (var fKjeoh in this.FIeFfN) { cPJhlM['_' + this.FIeFfN[fKjeoh][0]] = fKjeoh; };
                        var dPFKlj = '';
                        var ljmKpp = this.HKloFm(this.jemKaO);
                        var LNdPFc = this.cDHGgP(fNbdEN);
                        if (LNdPFc[0] > ljmKpp[0]) {
                            if (LNdPFc[1] > ljmKpp[1]) {
                                for (cJcdCM = 0; cJcdCM < 7; cJcdCM++) {
                                    ljmKpp[0] = ljmKpp[0] + 1;
                                    ljmKpp[1] = ljmKpp[1] + 1;
                                    if (ljmKpp[0] >= LNdPFc[0] && ljmKpp[1] >= LNdPFc[1]) { break; };
                                    FKfcOk = '_' + Math.round(ljmKpp[0] + (ljmKpp[1] * 8));
                                    if (cPJhlM[FKfcOk]) { this.acaemD = cPJhlM[FKfcOk]; break; }
                                };
                            } else {
                                for (cJcdCM = 0; cJcdCM < 7; cJcdCM++) {
                                    ljmKpp[0] = ljmKpp[0] + 1;
                                    ljmKpp[1] = ljmKpp[1] - 1;
                                    if (ljmKpp[0] >= LNdPFc[0] && ljmKpp[1] <= LNdPFc[1]) { break; };
                                    FKfcOk = '_' + Math.round(ljmKpp[0] + (ljmKpp[1] * 8));
                                    if (cPJhlM[FKfcOk]) { this.acaemD = cPJhlM[FKfcOk]; break; }
                                };
                            }
                        } else {
                            if (LNdPFc[1] > ljmKpp[1]) {
                                for (cJcdCM = 0; cJcdCM < 7; cJcdCM++) {
                                    ljmKpp[0] = ljmKpp[0] - 1;
                                    ljmKpp[1] = ljmKpp[1] + 1;
                                    if (ljmKpp[0] <= LNdPFc[0] && ljmKpp[1] >= LNdPFc[1]) { break; };
                                    FKfcOk = '_' + Math.round(ljmKpp[0] + (ljmKpp[1] * 8));
                                    if (cPJhlM[FKfcOk]) { this.acaemD = cPJhlM[FKfcOk]; break; }
                                };
                            } else {
                                for (cJcdCM = 0; cJcdCM < 7; cJcdCM++) {
                                    ljmKpp[0] = ljmKpp[0] - 1;
                                    ljmKpp[1] = ljmKpp[1] - 1;
                                    if (ljmKpp[0] <= LNdPFc[0] && ljmKpp[1] <= LNdPFc[1]) { break; };
                                    FKfcOk = '_' + Math.round(ljmKpp[0] + (ljmKpp[1] * 8));
                                    if (cPJhlM[FKfcOk]) { this.acaemD = cPJhlM[FKfcOk]; break; }
                                };
                            }
                        };
                        if (this.acaemD == '') { this.dNNHfe = false; }
                    };
                    if (this.BIAnlc > 20) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
                    this.JPfdKP.adBDen(this.AJBHGO);
                    if (this.dNNHfe) { this.AJBHGO.hMfInb.hIHeHD = false; } else {
                        this.AJBHGO.hMfInb.hIHeHD = true;
                        LLFKph.LKkafb(JLJeih + 'move', 1, false, 0, true);
                    };
                    if (this.acaemD != '') {
                        var mnfIoP = dCibpa(this.acaemD.substring(1));
                        if (mnfIoP < 21) { JLJeih = this.GhMInF; } else { JLJeih = this.NdeLeg; };
                        LLFKph.LKkafb(JLJeih + 'kill', 1, false, 0, true);
                    }
                } else { this.njcLkJ(); }
            };
        };
        hJEkmd.prototype.BAAkAa = function() {
            if (!this.OFPgOl) { return; };
            if (this.AJBHGO) {
                this.mHolDN = this.mHolDN + BLAZE.afEDBA.ddnjdC;
                if (this.mHolDN < this.DnGDMp) {
                    this.IEeIMH = (this.mHolDN / this.DnGDMp) * this.bJiMEP;
                    var pehbDg = AEOgJp.kDMBPo(this.aKbblp, this.IEeIMH / this.bJiMEP);
                    AEOgJp.pjMFnl(pehbDg, this.jemKaO);
                    if (this.dNNHfe) {
                        var NbgEcL = Math.abs(this.IEeIMH - this.GfihNB);
                        NbgEcL = bjAFpk - (bjAFpk * NbgEcL * NbgEcL * this.McLJef);
                        pehbDg[1] = pehbDg[1] - NbgEcL;
                    };
                    this.AJBHGO.ooLIDD = pehbDg;
                    this.JPfdKP.jeEAJP();
                    return;
                };
                this.AJBHGO.ooLIDD = this.HPiFCa;
            };
            this.njcLkJ();
            this.JPfdKP.jeEAJP();
        };
        hJEkmd.prototype.GCgkeK = function(KcMelf) {
            var hKPAKA = KcMelf.target;
            if (KcMelf.type == 'touchend') {
                if (KcMelf.changedTouches.length < 1) { return; };
                var nJogbk = KcMelf.changedTouches[0];
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                hKPAKA = document.elementFromPoint(nJogbk.clientX, nJogbk.clientY);
            } else if (KcMelf.type == 'touchstart') {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
            };
            if (!hKPAKA) { return; };
            if (!hKPAKA.parentNode) { return; };
            if (!hKPAKA.parentNode.eoIjGL) { return; };
            hKPAKA.parentNode.eoIjGL.ppCDLa(KcMelf.type, hKPAKA.kCmaeC);
        };
        hJEkmd.prototype.ppCDLa = function(fogfBH, kCmaeC) {
            if (this.nlemFe) { this.GilbBF(); return; };
            if (!this.aiIcIi || !this.aGEjAM.cOPbiG || this.OFPgOl || this.fjdCgI < 1) { return; };
            kCmaeC = dCibpa(kCmaeC);
            var iBamkN, JLJeih;
            var MlnmKA = kCmaeC % 8;
            var HloEke = (kCmaeC - MlnmKA) / 8;
            if (this.jDChHC == 1) {
                iBamkN = HloEke;
                HloEke = MlnmKA;
                MlnmKA = 7 - iBamkN;
            } else if (this.jDChHC == 2) {
                iBamkN = HloEke;
                HloEke = 7 - MlnmKA;
                MlnmKA = iBamkN;
            };
            kCmaeC = HloEke * 8 + MlnmKA;
            if (this.LBkPnh(kCmaeC)) { return; };
            var aCHjkF = 0;
            for (var KgDnNJ in this.FIeFfN) { if (this.FIeFfN[KgDnNJ][0] == kCmaeC) { aCHjkF = dCibpa(KgDnNJ.substring(1)); break; } };
            this.iMEbme(this.fjdCgI, false);
            if (this.fHNDkc == 0) {
                if (fogfBH == 'mousedown' || fogfBH == 'touchstart') {
                    if (aCHjkF > 0) {
                        if (this.fjdCgI == 1) {
                            if (aCHjkF > 20) { return; };
                            JLJeih = this.NdeLeg;
                        } else if (this.fjdCgI == 2) {
                            if (aCHjkF < 21) { return; };
                            JLJeih = this.GhMInF;
                        } else { return; };
                        LLFKph.LKkafb(JLJeih + 'click', 1, false, 0, true);
                        this.BgCLbl = [];
                        this.fHNDkc = aCHjkF;
                        this.nKdkCL = kCmaeC;
                        this.aPiOCB(kCmaeC);
                        this.kOcLKF = this.BiipIN(this.fHNDkc);
                        if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); }
                    };
                }
            } else {
                if (fogfBH == 'mousedown' || fogfBH == 'touchstart') {
                    if (!this.gAOEgM) {
                        if (this.fHNDkc == aCHjkF || this.nKdkCL == kCmaeC) {} else {
                            if (aCHjkF > 0) {
                                if (this.fjdCgI == 1) {
                                    if (aCHjkF > 20) { return; };
                                    JLJeih = this.NdeLeg;
                                } else if (this.fjdCgI == 2) {
                                    if (aCHjkF < 21) { return; };
                                    JLJeih = this.GhMInF;
                                } else { return; };
                                this.BgCLbl = [];
                                this.fHNDkc = aCHjkF;
                                this.nKdkCL = kCmaeC;
                                this.aPiOCB(kCmaeC);
                                this.kOcLKF = this.BiipIN(this.fHNDkc);
                                if (this.AbOpkd) { this.hEPkfB(this.kOcLKF.aeDnaK); };
                                LLFKph.LKkafb(JLJeih + 'click', 1, false, 0, true);
                            }
                        };
                    }
                } else if (fogfBH == 'mouseup' || fogfBH == 'touchend') {
                    if (aCHjkF == 0) {
                        if (this.kOcLKF) {
                            var hnmECj = '_' + kCmaeC;
                            if (this.kOcLKF.hasOwnProperty(hnmECj)) {
                                this.BgCLbl.push(kCmaeC);
                                this.hEPkfB([]);
                                this.ckIaEI([
                                    [this.fHNDkc, kCmaeC]
                                ]);
                                var aDlnMk = this.kOcLKF[hnmECj];
                                var EcEKIB = false;
                                if (aDlnMk > 0) { aDlnMk = '_' + aDlnMk; if (this.FIeFfN[aDlnMk]) { delete this.FIeFfN[aDlnMk]; } } else { EcEKIB = true; };
                                this.FIeFfN['_' + this.fHNDkc][0] = kCmaeC;
                                if (!EcEKIB) { if (this.oECmEe[1] == 'amcheckers') { if (this.FIeFfN['_' + this.fHNDkc][1] == 0) { var KndDFa = this.cDHGgP(kCmaeC); if (this.fjdCgI == 1) { EcEKIB = KndDFa[0] == 7; } else { EcEKIB = KndDFa[0] == 0; } }; } };
                                if (!EcEKIB) {
                                    this.bhlHJO = null;
                                    this.iMEbme(this.fjdCgI, true);
                                    this.kOcLKF = this.BiipIN(this.fHNDkc);
                                    if (this.kOcLKF.aeDnaK.length > 0 && this.kOcLKF.aDlnMk) {
                                        this.gAOEgM = true;
                                        this.aPiOCB(kCmaeC);
                                        return;
                                    }
                                };
                                this.kOcLKF = null;
                                this.bhlHJO = null;
                                this.fjdCgI = 0;
                                this.PMiHiP();
                                this.JKdCgI.pPEGkJ({ c: 'move', v: this.fHNDkc + ':' + this.BgCLbl.join(':') });
                                this.BgCLbl = [];
                                this.JKdCgI.BNkojA();
                            }
                        };
                    }
                };
            }
        };
        hJEkmd.prototype.BiipIN = function(aCHjkF) { if (this.bhlHJO) { var KgDnNJ = '_' + aCHjkF; if (this.bhlHJO[KgDnNJ]) { return this.bhlHJO[KgDnNJ]; } }; return { aeDnaK: [], aDlnMk: false }; };
        hJEkmd.prototype.iMEbme = function(kEJgnC, NneaaE) {
            if (this.bhlHJO) { return; };
            this.bhlHJO = {};
            var cJcdCM, cIhEIM, KgDnNJ, aCHjkF;
            var iCjDFG = [];
            var cPJhlM = {};
            for (KgDnNJ in this.FIeFfN) {
                aCHjkF = dCibpa(KgDnNJ.substring(1));
                cPJhlM['_' + this.FIeFfN[KgDnNJ][0]] = aCHjkF;
                if (kEJgnC == 1) { if (aCHjkF < 21) { iCjDFG.push(aCHjkF); } } else { if (aCHjkF > 20) { iCjDFG.push(aCHjkF); } };
            };
            var ajOcDd = false;
            cIhEIM = iCjDFG.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                aCHjkF = iCjDFG[cJcdCM];
                KgDnNJ = '_' + aCHjkF;
                this.bhlHJO[KgDnNJ] = this.MPMEim(aCHjkF, cPJhlM, NneaaE);
                if (this.bhlHJO[KgDnNJ].aDlnMk) { ajOcDd = true; }
            };
            if (ajOcDd) { for (KgDnNJ in this.bhlHJO) { var hegNOA = this.bhlHJO[KgDnNJ]; if (!hegNOA.aDlnMk) { if (hegNOA.aeDnaK.length > 0) { this.bhlHJO[KgDnNJ] = { aeDnaK: [], aDlnMk: false }; } }; } };
        };
        hJEkmd.prototype.MPMEim = function(aCHjkF, cPJhlM, NneaaE) {
            var cJcdCM, cIhEIM, fKjeoh, FKfcOk, cFakob, fOdCAD, nIoPJO, KgDnNJ, GGacAl, NbgEcL, lhFlLE;
            var ofMhiD = this.oECmEe[1];
            var gceHgN = { aeDnaK: [], aDlnMk: false };
            KgDnNJ = '_' + aCHjkF;
            if (!this.FIeFfN[KgDnNJ]) { return; };
            var PFInhD = this.FIeFfN[KgDnNJ][0];
            var ljmKpp = this.cDHGgP(PFInhD);
            var CPKMOI = this.FIeFfN[KgDnNJ][1] > 0;
            var jMDjil = aCHjkF < 21;
            var AdlFOn, jCHLkG;
            if (ofMhiD == 'gzcheckers' || ofMhiD == 'anticheckers') {
                if (CPKMOI) {
                    this.HnmLLO([-1, -1], jMDjil, ljmKpp, gceHgN, cPJhlM, false);
                    this.HnmLLO([-1, 1], jMDjil, ljmKpp, gceHgN, cPJhlM, false);
                    this.HnmLLO([1, -1], jMDjil, ljmKpp, gceHgN, cPJhlM, false);
                    this.HnmLLO([1, 1], jMDjil, ljmKpp, gceHgN, cPJhlM, false);
                    if (gceHgN.aDlnMk) {
                        var Jdjkoi = { aeDnaK: [], aDlnMk: true };
                        for (fKjeoh in gceHgN) {
                            if (fKjeoh.substring(0, 1) == '_') {
                                if (gceHgN[fKjeoh] > 0) {
                                    Jdjkoi[fKjeoh] = gceHgN[fKjeoh];
                                    Jdjkoi.aeDnaK.push(dCibpa(fKjeoh.substring(1)));
                                }
                            };
                        };
                        gceHgN = Jdjkoi;
                    }
                } else {
                    AdlFOn = [
                        [1, -1],
                        [1, 1]
                    ];
                    jCHLkG = [
                        [2, -2, -7],
                        [2, 2, 9],
                        [-2, -2, -9],
                        [-2, 2, 7]
                    ];
                    cIhEIM = jCHLkG.length;
                    for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                        NbgEcL = jCHLkG[cJcdCM];
                        if (jMDjil) { nIoPJO = PFInhD + NbgEcL[2]; } else {
                            AEOgJp.oCMmhm(NbgEcL);
                            nIoPJO = PFInhD - NbgEcL[2];
                        };
                        GGacAl = AEOgJp.olNCjJ(ljmKpp, NbgEcL);
                        if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                        if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                        cFakob = GGacAl[1] * 8 + GGacAl[0];
                        FKfcOk = '_' + cFakob;
                        fOdCAD = '_' + nIoPJO;
                        if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                            if (cPJhlM.hasOwnProperty(fOdCAD)) {
                                fKjeoh = cPJhlM[fOdCAD];
                                if (jMDjil) { if (fKjeoh < 21) { continue; } } else { if (fKjeoh > 20) { continue; } };
                                gceHgN.aDlnMk = true;
                                gceHgN[FKfcOk] = fKjeoh;
                                gceHgN.aeDnaK.push(cFakob);
                            }
                        };
                    };
                    if (!gceHgN.aDlnMk) {
                        cIhEIM = AdlFOn.length;
                        for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                            NbgEcL = AdlFOn[cJcdCM];
                            if (!jMDjil) { AEOgJp.oCMmhm(NbgEcL); };
                            GGacAl = AEOgJp.olNCjJ(ljmKpp, NbgEcL);
                            if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                            if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                            cFakob = GGacAl[1] * 8 + GGacAl[0];
                            FKfcOk = '_' + cFakob;
                            if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                                gceHgN[FKfcOk] = 0;
                                gceHgN.aeDnaK.push(cFakob);
                            }
                        };
                    }
                };
            } else if (ofMhiD == 'amcheckers') {
                if (CPKMOI) {
                    AdlFOn = [
                        [1, -1],
                        [1, 1],
                        [-1, 1],
                        [-1, -1]
                    ];
                    jCHLkG = [
                        [2, -2, -7],
                        [2, 2, 9],
                        [-2, -2, -9],
                        [-2, 2, 7]
                    ];
                } else {
                    AdlFOn = [
                        [1, -1],
                        [1, 1]
                    ];
                    if (NneaaE) {
                        jCHLkG = [
                            [2, -2, -7],
                            [2, 2, 9],
                            [-2, -2, -9],
                            [-2, 2, 7]
                        ];
                    } else {
                        jCHLkG = [
                            [2, -2, -7],
                            [2, 2, 9]
                        ];
                    }
                };
                cIhEIM = jCHLkG.length;
                for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    NbgEcL = jCHLkG[cJcdCM];
                    if (jMDjil) { nIoPJO = PFInhD + NbgEcL[2]; } else {
                        AEOgJp.oCMmhm(NbgEcL);
                        nIoPJO = PFInhD - NbgEcL[2];
                    };
                    GGacAl = AEOgJp.olNCjJ(ljmKpp, NbgEcL);
                    if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                    if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                    cFakob = GGacAl[1] * 8 + GGacAl[0];
                    FKfcOk = '_' + cFakob;
                    fOdCAD = '_' + nIoPJO;
                    if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                        if (cPJhlM.hasOwnProperty(fOdCAD)) {
                            fKjeoh = cPJhlM[fOdCAD];
                            if (jMDjil) { if (fKjeoh < 21) { continue; } } else { if (fKjeoh > 20) { continue; } };
                            gceHgN.aDlnMk = true;
                            gceHgN[FKfcOk] = fKjeoh;
                            gceHgN.aeDnaK.push(cFakob);
                        }
                    };
                };
                if (!gceHgN.aDlnMk) {
                    cIhEIM = AdlFOn.length;
                    for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                        NbgEcL = AdlFOn[cJcdCM];
                        if (!jMDjil) { AEOgJp.oCMmhm(NbgEcL); };
                        GGacAl = AEOgJp.olNCjJ(ljmKpp, NbgEcL);
                        if (GGacAl[0] < 0 || GGacAl[0] > 7) { continue; };
                        if (GGacAl[1] < 0 || GGacAl[1] > 7) { continue; };
                        cFakob = GGacAl[1] * 8 + GGacAl[0];
                        FKfcOk = '_' + cFakob;
                        if (!cPJhlM.hasOwnProperty(FKfcOk)) {
                            gceHgN[FKfcOk] = 0;
                            gceHgN.aeDnaK.push(cFakob);
                        }
                    };
                }
            };
            return gceHgN;
        };
        hJEkmd.prototype.HnmLLO = function(NbgEcL, jMDjil, ljmKpp, gceHgN, cPJhlM, ACobhC) {
            var nFJBPd = {};
            var baINOG = [];
            var lhFlLE = 0;
            var cJcdCM, cIhEIM, fKjeoh, fgEAcn, cFakob, FKfcOk, KndDFa = AEOgJp.clhoEK(ljmKpp);
            for (cJcdCM = 0; cJcdCM < 7; cJcdCM++) {
                AEOgJp.pjMFnl(KndDFa, NbgEcL);
                if (KndDFa[0] > 7 || KndDFa[0] < 0) { break; };
                if (KndDFa[1] > 7 || KndDFa[1] < 0) { break; };
                cFakob = Math.round(KndDFa[0] + (KndDFa[1] * 8));
                FKfcOk = '_' + cFakob;
                if (cPJhlM.hasOwnProperty(FKfcOk)) { if (lhFlLE <= 0) { lhFlLE = cPJhlM[FKfcOk]; if (jMDjil) { if (lhFlLE < 21) { break; } } else { if (lhFlLE > 20) { break; } }; } else { break; } } else {
                    if (lhFlLE > 0) { gceHgN.aDlnMk = true; };
                    nFJBPd[FKfcOk] = lhFlLE;
                    baINOG.push(cFakob);
                }
            };
            if (!ACobhC) {
                if (gceHgN.aDlnMk) {
                    var HjANkG = null;
                    baINOG = [];
                    fgEAcn = Object.keys(nFJBPd);
                    cIhEIM = fgEAcn.length;
                    for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                        fKjeoh = fgEAcn[cJcdCM];
                        if (nFJBPd[fKjeoh] > 0) {
                            cFakob = dCibpa(fKjeoh.substring(1));
                            var GGacAl = this.cDHGgP(cFakob);
                            var OPedaH = { aeDnaK: [], aDlnMk: false };
                            if (NbgEcL[0] != 1 || NbgEcL[1] != 1) { this.HnmLLO([-1, -1], jMDjil, GGacAl, OPedaH, cPJhlM, true); };
                            if (NbgEcL[0] != 1 || NbgEcL[1] != -1) { this.HnmLLO([-1, 1], jMDjil, GGacAl, OPedaH, cPJhlM, true); };
                            if (NbgEcL[0] != -1 || NbgEcL[1] != 1) { this.HnmLLO([1, -1], jMDjil, GGacAl, OPedaH, cPJhlM, true); };
                            if (NbgEcL[0] != -1 || NbgEcL[1] != -1) { this.HnmLLO([1, 1], jMDjil, GGacAl, OPedaH, cPJhlM, true); };
                            if (OPedaH.aDlnMk) {
                                if (!HjANkG) { HjANkG = {}; };
                                HjANkG[fKjeoh] = true;
                            };
                            baINOG.push(cFakob);
                        } else { delete nFJBPd[fKjeoh]; }
                    };
                    if (HjANkG) {
                        baINOG = [];
                        fgEAcn = Object.keys(nFJBPd);
                        cIhEIM = fgEAcn.length;
                        for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { fKjeoh = fgEAcn[cJcdCM]; if (HjANkG.hasOwnProperty(fKjeoh)) { baINOG.push(dCibpa(fKjeoh.substring(1))); } else { delete nFJBPd[fKjeoh]; } };
                    }
                };
            };
            for (fKjeoh in nFJBPd) { gceHgN[fKjeoh] = nFJBPd[fKjeoh]; };
            cIhEIM = baINOG.length;
            for (cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { gceHgN.aeDnaK.push(baINOG[cJcdCM]); }
        };
        return function() { return new aGEjAM(new hJEkmd(arguments)) };
    })();
    BLAZE.NjLaCP = NjLaCP;
    var ojABhi = (function() {
        var aaPJke = BLAZE.GetENV('PROJECT_CONTENT_URL');
        var MLBlFB = 10000;
        var LmbbBH = Math.round(MLBlFB * 0.1);
        var OHLmpM = 1 / MLBlFB;
        var FFkHeK = 1.3;
        var elpaPi = 2.7;
        var lAAAEb = 0.7;
        var mJJNfN = [12, 10];
        var DMoHbb = mJJNfN[0] * mJJNfN[1];
        var oEAdfk = HiMfgN.cGgNAb(1.5 * MLBlFB);
        var ahDlEp = 0.7;
        var hlKMBI = 6;
        var mDGpen = (1 - ahDlEp) / hlKMBI;
        var LnBhIE = 1 / hlKMBI;
        var AaKhBc = 10;
        var BJHIIA = 160;
        var jAhiko = 20;
        var PEiBck = 1 * MLBlFB;
        var pOIhMH = 100;
        var ChIgGP = 0.5;
        var faegaG = 1.2;
        var JghLjP = [160, 1140];
        var ekJaln = 26;
        var bDeDeB = 220;
        var eBMKhc = 1.7;
        var hLGAig = 0.004;
        var CFeCBn = 0.1;
        var EHncnf = 200;
        var dDCPoE = 1.2;
        var lEaKoD = 2;
        var FcKhHG = 5;
        var MmhAhP = { lLPBaL: ['pocket_1', 'pocket_2', 'pocket_3', 'pocket_4'], CjnLhN: ['cue'], LbbgNE: ['table_border'], cFaMeP: ['ball_s1', 'ball_s2', 'ball_s3', 'ball_s4'], NOmIgn: ['ball_m1', 'ball_m2', 'ball_m3', 'ball_m4', 'ball_m5'], jkhnCa: ['ball_f1', 'ball_f2', 'ball_f3', 'ball_f4', 'ball_f5'] };
        var nAhdFd = [
            ['10% 100%'],
            ['10% 0%'],
            ['20% 100%'],
            ['20% 0%'],
            ['30% 100%'],
            ['30% 0%'],
            ['40% 100%'],
            ['40% 0%'],
            ['50% 100%'],
            ['50% 0%'],
            ['60% 100%'],
            ['60% 0%'],
            ['70% 100%'],
            ['70% 0%'],
            ['80% 100%'],
            ['80% 0%'],
            ['90% 100%'],
            ['90% 0%'],
            ['100% 100%'],
            ['100% 0%']
        ];
        var cmkjdC = [];
        cmkjdC[1] = [60.9, 0.032, true, nAhdFd];
        cmkjdC[2] = [49.4, 0.04, true, nAhdFd];
        cmkjdC[3] = [41.54, 0.048, true, nAhdFd];
        cmkjdC[4] = [37.6, 0.04, true, nAhdFd];
        cmkjdC[5] = [34.1, 0.035, true, nAhdFd];
        cmkjdC[6] = [13.25, 0.04, true, nAhdFd];
        cmkjdC[7] = [23.38, 0.03, true, nAhdFd];
        var BgGFbP = [1800, 1000];
        var gInEBG = [7, 4];
        var FibKcf = [BgGFbP[0] * MLBlFB, BgGFbP[1] * MLBlFB];
        var NcFLDH = [Math.round(FibKcf[0] / gInEBG[0]), Math.round(FibKcf[1] / gInEBG[1])];
        var KEfDLO = 'billiards_ballset';
        var ImeeDd = [5, 3];
        var gOcDCD = [];
        gOcDCD[0] = {
            OaahBD: 25,
            pEcedm: [
                [1, 0],
                [2, 1],
                [3, 2],
                [4, 3],
                [5, 4],
                [6, 5],
                [7, 6],
                [8, 7],
                [9, 8],
                [1, 9],
                [1, 10],
                [1, 11],
                [1, 12],
                [1, 13],
                [1, 14],
                [1, 15]
            ]
        };
        gOcDCD[1] = {
            OaahBD: 25,
            pEcedm: [
                [1, 0],
                [2, 1],
                [3, 2],
                [4, 3],
                [5, 4],
                [6, 5],
                [7, 6],
                [8, 7],
                [9, 8],
                [1, 9],
                [1, 10],
                [1, 11],
                [1, 12],
                [1, 13],
                [1, 14],
                [1, 15]
            ]
        };
        gOcDCD[2] = {
            OaahBD: 27,
            pEcedm: [
                [14, 0],
                [1, 1],
                [1, 2],
                [1, 3],
                [1, 4],
                [1, 5],
                [1, 6],
                [1, 7],
                [1, 8],
                [1, 16],
                [1, 17],
                [1, 18],
                [1, 19],
                [1, 20],
                [1, 21],
                [1, 22]
            ]
        };
        gOcDCD[3] = {
            OaahBD: 26,
            pEcedm: [
                [1, 0],
                [14, -1],
                [10, -1]
            ]
        };
        gOcDCD[4] = {
            OaahBD: 25,
            pEcedm: [
                [1, 0],
                [2, 1],
                [3, 2],
                [4, 3],
                [5, 4],
                [6, 5],
                [7, 6],
                [8, 7],
                [9, 8],
                [1, 9]
            ]
        };
        gOcDCD[5] = {
            OaahBD: 22,
            pEcedm: [
                [1, 0],
                [2, -1],
                [7, -1],
                [6, -1],
                [3, -1],
                [13, -1],
                [9, -1],
                [12, -1],
                [11, -1],
                [10, -1]
            ]
        };
        gOcDCD[6] = {
            OaahBD: 25,
            pEcedm: [
                [1, 0],
                [10, -1],
                [10, -1],
                [10, -1],
                [10, -1],
                [10, -1],
                [9, -1],
                [9, -1],
                [9, -1],
                [9, -1],
                [9, -1],
                [14, -1],
                [14, -1],
                [14, -1],
                [14, -1],
                [14, -1]
            ]
        };
        var JlCeOh = [];
        JlCeOh[0] = {
            lcFaFD: 0,
            GAPjel: 0,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 4990000],
                [5670000, 5000000],
                [5210000, 4730000],
                [5210000, 5270000],
                [4740000, 4460000],
                [4760000, 5000000],
                [4740000, 5530000],
                [4280000, 4200000],
                [4300000, 4730000],
                [4300000, 5270000],
                [4280000, 5800000],
                [3820000, 3940000],
                [3830000, 4470000],
                [3840000, 5000000],
                [3830000, 5530000],
                [3820000, 6060000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, 5],
                [9, 9, -1],
                [10, 10, -1],
                [11, 11, -1],
                [12, 12, -1],
                [13, 13, -1],
                [14, 14, -1],
                [15, 15, -1]
            ]
        };
        JlCeOh[1] = {
            lcFaFD: 1,
            GAPjel: 1,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 4990000],
                [5670000, 5000000],
                [5210000, 4730000],
                [5210000, 5270000],
                [4740000, 4460000],
                [4760000, 5000000],
                [4740000, 5530000],
                [4280000, 4200000],
                [4300000, 4730000],
                [4300000, 5270000],
                [4280000, 5800000],
                [3820000, 3940000],
                [3830000, 4470000],
                [3840000, 5000000],
                [3830000, 5530000],
                [3820000, 6060000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, -1],
                [9, 9, -1],
                [10, 10, -1],
                [11, 11, -1],
                [12, 12, -1],
                [13, 13, -1],
                [14, 14, -1],
                [15, 15, -1]
            ]
        };
        JlCeOh[2] = {
            lcFaFD: 2,
            GAPjel: 2,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 4990000],
                [5790000, 5000000],
                [5300000, 4710000],
                [5300000, 5290000],
                [4800000, 4420000],
                [4820000, 5000000],
                [4800000, 5570000],
                [4310000, 4140000],
                [4330000, 4710000],
                [4330000, 5290000],
                [4310000, 5860000],
                [3820000, 3860000],
                [3830000, 4430000],
                [3840000, 5000000],
                [3830000, 5570000],
                [3820000, 6140000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, -1],
                [9, 9, -1],
                [10, 10, -1],
                [11, 11, -1],
                [12, 12, -1],
                [13, 13, -1],
                [14, 14, -1],
                [15, 15, -1]
            ]
        };
        JlCeOh[3] = {
            lcFaFD: 3,
            GAPjel: 3,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13125000, 5000000],
                [4850000, 5000000],
                [4850000, 3720000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, 1],
                [2, 2, 2]
            ]
        };
        JlCeOh[4] = {
            lcFaFD: 4,
            GAPjel: 0,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [9000000, 6460000],
                [9000000, 4850000],
                [9270000, 4400000],
                [8730000, 4400000],
                [9530000, 3940000],
                [9000000, 3950000],
                [8470000, 3940000],
                [9780000, 3470000],
                [9260000, 3490000],
                [8740000, 3490000],
                [8220000, 3470000],
                [10040000, 3010000],
                [9520000, 3020000],
                [9000000, 3010000],
                [8480000, 3020000],
                [7960000, 3010000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, -1],
                [9, 9, -1],
                [10, 10, -1],
                [11, 11, -1],
                [12, 12, -1],
                [13, 13, -1],
                [14, 14, -1],
                [15, 15, -1]
            ]
        };
        JlCeOh[5] = {
            lcFaFD: 5,
            GAPjel: 5,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 1.4,
            foLokD: [
                [14700000, 5000000],
                [13150000, 3420000],
                [13150000, 6580000],
                [13150000, 5000000],
                [9000000, 5000000],
                [5870000, 5000000],
                [2220000, 5000000],
                [5390000, 5000000],
                [4980000, 4760000],
                [4980000, 5240000],
                [4570000, 4530000],
                [4580000, 5000000],
                [4570000, 5470000],
                [4160000, 4280000],
                [4170000, 4760000],
                [4170000, 5240000],
                [4160000, 5720000],
                [3750000, 4060000],
                [3760000, 4530000],
                [3750000, 5000000],
                [3760000, 5470000],
                [3750000, 5940000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, 1],
                [2, 2, 2],
                [3, 3, 3],
                [4, 4, 4],
                [5, 5, 5],
                [6, 6, 6],
                [7, 9, -1],
                [8, 9, -1],
                [9, 9, -1],
                [10, 9, -1],
                [11, 9, -1],
                [12, 9, -1],
                [13, 9, -1],
                [14, 9, -1],
                [15, 9, -1],
                [16, 9, -1],
                [17, 9, -1],
                [18, 9, -1],
                [19, 9, -1],
                [20, 9, -1],
                [21, 9, -1]
            ]
        };
        JlCeOh[6] = {
            lcFaFD: 5,
            GAPjel: 5,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 1.4,
            foLokD: [
                [14700000, 5000000],
                [13150000, 3420000],
                [13150000, 6580000],
                [13150000, 5000000],
                [9000000, 5000000],
                [5870000, 5000000],
                [2220000, 5000000],
                [7430000, 5000000],
                [10570000, 5000000],
                [5390000, 5000000],
                [4980000, 4760000],
                [4980000, 5240000],
                [4570000, 4530000],
                [4580000, 5000000],
                [4570000, 5470000],
                [4160000, 4280000],
                [4170000, 4760000],
                [4170000, 5240000],
                [4160000, 5720000],
                [3750000, 4060000],
                [3760000, 4530000],
                [3750000, 5000000],
                [3760000, 5470000],
                [3750000, 5940000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, 1],
                [2, 2, 2],
                [3, 3, 3],
                [4, 4, 4],
                [5, 5, 5],
                [6, 6, 6],
                [7, 7, 7],
                [8, 8, 8],
                [9, 9, -1],
                [10, 9, -1],
                [11, 9, -1],
                [12, 9, -1],
                [13, 9, -1],
                [14, 9, -1],
                [15, 9, -1],
                [16, 9, -1],
                [17, 9, -1],
                [18, 9, -1],
                [19, 9, -1],
                [20, 9, -1],
                [21, 9, -1],
                [22, 9, -1],
                [23, 9, -1]
            ]
        };
        JlCeOh[7] = {
            lcFaFD: 0,
            GAPjel: 4,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 5000000],
                [5670000, 5000000],
                [4300000, 5260000],
                [4750000, 4470000],
                [3840000, 5000000],
                [5210000, 5260000],
                [4300000, 4740000],
                [5210000, 4740000],
                [4750000, 5530000],
                [4760000, 5000000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, 1],
                [2, 2, 2],
                [3, 3, 3],
                [4, 4, 4],
                [5, 5, 5],
                [6, 6, 6],
                [7, 7, 7],
                [8, 8, 8],
                [9, 9, 9]
            ]
        };
        JlCeOh[8] = {
            lcFaFD: 0,
            GAPjel: 6,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 4990000],
                [5670000, 5000000],
                [5210000, 4730000],
                [5210000, 5270000],
                [4740000, 4460000],
                [4760000, 5000000],
                [4740000, 5530000],
                [4280000, 4200000],
                [4300000, 4730000],
                [4300000, 5270000],
                [4280000, 5800000],
                [3820000, 3940000],
                [3830000, 4470000],
                [3840000, 5000000],
                [3830000, 5530000],
                [3820000, 6060000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, 5],
                [9, 9, -1],
                [10, 10, -1],
                [11, 11, -1],
                [12, 12, -1],
                [13, 13, -1],
                [14, 14, -1],
                [15, 15, -1]
            ]
        };
        JlCeOh[9] = {
            lcFaFD: 0,
            GAPjel: 4,
            FKbhkM: 45,
            gfljHJ: 1.2,
            BLPCKm: 0.13,
            KGnkFL: 2.0,
            foLokD: [
                [13477000, 5000000],
                [5670000, 5000000],
                [4300000, 5260000],
                [4750000, 4470000],
                [3840000, 5000000],
                [5210000, 5260000],
                [4300000, 4740000],
                [5210000, 4740000],
                [4750000, 5530000],
                [4760000, 5000000]
            ],
            pEcedm: [
                [0, 0, 0],
                [1, 1, -1],
                [2, 2, -1],
                [3, 3, -1],
                [4, 4, -1],
                [5, 5, -1],
                [6, 6, -1],
                [7, 7, -1],
                [8, 8, -1],
                [9, 9, -1]
            ]
        };
        var iNcCoK = [];
        iNcCoK[0] = {
            AIONko: 45,
            diBAcc: [
                [1030000, 1030000],
                [16970000, 8970000]
            ],
            PcpKAg: [
                [13130000, 1030000],
                [16970000, 8970000]
            ],
            IPMfPb: [
                [13120000, 5000000],
                [13120000, 3420000]
            ],
            GhfCLm: { _1: [980000, 980000], _2: [980000, 9020000], _3: [9000000, 750000], _4: [9000000, 9250000], _5: [17020000, 980000], _6: [17020000, 9020000] },
            OMLdpH: { _1: [635000, 635000], _3: [9000000, 390000], _5: [17365000, 635000], _6: [17365000, 9365000], _4: [9000000, 9610000], _2: [635000, 9365000] },
            lLgpbF: [
                [1000000, 1280000, 0, -70000, 20000, 44400000000, 72801.09889280518],
                [980000, 1210000, 0, -270000, 270000, -62100000000, 381837.66184073564],
                [710000, 940000, 1, -230000, -230000, 379500000000, 325269.11934581184],
                [940000, 710000, 0, 270000, -270000, -62100000000, 381837.66184073564],
                [1210000, 980000, 0, 20000, -70000, 44400000000, 72801.09889280518],
                [1280000, 1000000, 0, 0, -7320000, 7320000000000, 7320000],
                [8600000, 1000000, 0, -80000, -110000, 798000000000, 136014.70508735444],
                [8710000, 920000, 0, -330000, -70000, 2938700000000, 337342.55586866],
                [8780000, 590000, 3, 0, -440000, 259600000000, 440000],
                [9220000, 590000, 0, 330000, -70000, -3001300000000, 337342.55586866],
                [9290000, 920000, 0, 80000, -110000, -642000000000, 136014.70508735444],
                [9400000, 1000000, 0, 0, -7320000, 7320000000000, 7320000],
                [16720000, 1000000, 0, -20000, -70000, 404400000000, 72801.09889280518],
                [16790000, 980000, 0, -270000, -270000, 4797900000000, 381837.66184073564],
                [17060000, 710000, 5, 230000, -230000, -3760500000000, 325269.11934581184],
                [17290000, 940000, 0, 270000, 270000, -4922100000000, 381837.66184073564],
                [17020000, 1210000, 0, 70000, 20000, -1215600000000, 72801.09889280518],
                [17000000, 1280000, 0, 7440000, 0, -126480000000000, 7440000],
                [17000000, 8720000, 0, 70000, -20000, -1015600000000, 72801.09889280518],
                [17020000, 8790000, 0, 270000, -270000, -2222100000000, 381837.66184073564],
                [17290000, 9060000, 6, 230000, 230000, -6060500000000, 325269.11934581184],
                [17060000, 9290000, 0, -270000, 270000, 2097900000000, 381837.66184073564],
                [16790000, 9020000, 0, -20000, 70000, -295600000000, 72801.09889280518],
                [16720000, 9000000, 0, 0, 7320000, -65880000000000, 7320000],
                [9400000, 9000000, 0, 80000, 110000, -1742000000000, 136014.70508735444],
                [9290000, 9080000, 0, 330000, 70000, -3701300000000, 337342.55586866],
                [9220000, 9410000, 4, 0, 440000, -4140400000000, 440000],
                [8780000, 9410000, 0, -330000, 70000, 2238700000000, 337342.55586866],
                [8710000, 9080000, 0, -80000, 110000, -302000000000, 136014.70508735444],
                [8600000, 9000000, 0, 0, 7320000, -65880000000000, 7320000],
                [1280000, 9000000, 0, 20000, 70000, -655600000000, 72801.09889280518],
                [1210000, 9020000, 0, 270000, 270000, -2762100000000, 381837.66184073564],
                [940000, 9290000, 2, -230000, 230000, -1920500000000, 325269.11934581184],
                [710000, 9060000, 0, -270000, -270000, 2637900000000, 381837.66184073564],
                [980000, 8790000, 0, -70000, -20000, 244400000000, 72801.09889280518],
                [1000000, 8720000, 0, -7440000, 0, 7440000000000, 7440000],
                [1000000, 1280000, 0]
            ],
            lAAMfE: [
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [5, 0, 1, 2, 3, 4, 35],
                    [5],
                    [5], null, null, null, null, [5, 35],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [11, 5, 6, 7, 8, 9, 10],
                    [11],
                    [11], null, null, null, null, [11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11],
                    [11],
                    [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [35, 0, 1, 2, 3, 4, 5],
                    [35, 5], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [5],
                    [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5],
                    [5, 6, 7, 8, 9, 10, 11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [17, 11],
                    [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34],
                    [35, 29], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23],
                    [23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35],
                    [29],
                    [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [29], null, null, null, null, [29],
                    [29],
                    [29, 23, 24, 25, 26, 27, 28], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23, 17], null, null, null, null, [23],
                    [23],
                    [23, 17, 18, 19, 20, 21, 22]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ]
            ]
        };
        iNcCoK[1] = {
            AIONko: 55,
            diBAcc: [
                [1160000, 1160000],
                [16840000, 8840000]
            ],
            PcpKAg: [
                [13060000, 1160000],
                [16840000, 8840000]
            ],
            IPMfPb: [
                [13050000, 5000000],
                [13050000, 3150000]
            ],
            GhfCLm: { _1: [1150000, 1150000], _2: [1150000, 8850000], _3: [9000000, 900000], _4: [9000000, 9100000], _5: [16850000, 1150000], _6: [16850000, 8850000] },
            OMLdpH: { _1: [750000, 750000], _3: [9000000, 460000], _5: [17250000, 750000], _6: [17250000, 9250000], _4: [9000000, 9540000], _2: [750000, 9250000] },
            lLgpbF: [
                [1150000, 1420000, 0, -60000, 30000, 26400000000, 67082.03932499369],
                [1120000, 1360000, 0, -320000, 320000, -76800000000, 452548.3399593904],
                [800000, 1040000, 1, -240000, -240000, 441600000000, 339411.2549695428],
                [1040000, 800000, 0, 320000, -320000, -76800000000, 452548.3399593904],
                [1360000, 1120000, 0, 30000, -60000, 26400000000, 67082.03932499369],
                [1420000, 1150000, 0, 0, -7150000, 8222500000000, 7150000],
                [8570000, 1150000, 0, -90000, -110000, 897800000000, 142126.70403551895],
                [8680000, 1060000, 0, -410000, -100000, 3664800000000, 422018.95692018385],
                [8780000, 650000, 3, 0, -440000, 286000000000, 440000],
                [9220000, 650000, 0, 410000, -100000, -3715200000000, 422018.95692018385],
                [9320000, 1060000, 0, 90000, -110000, -722200000000, 142126.70403551895],
                [9430000, 1150000, 0, 0, -7150000, 8222500000000, 7150000],
                [16580000, 1150000, 0, -30000, -60000, 566400000000, 67082.03932499369],
                [16640000, 1120000, 0, -320000, -320000, 5683200000000, 452548.3399593904],
                [16960000, 800000, 5, 240000, -240000, -3878400000000, 339411.2549695428],
                [17200000, 1040000, 0, 320000, 320000, -5836800000000, 452548.3399593904],
                [16880000, 1360000, 0, 60000, 30000, -1053600000000, 67082.03932499369],
                [16850000, 1420000, 0, 7160000, 0, -120646000000000, 7160000],
                [16850000, 8580000, 0, 60000, -30000, -753600000000, 67082.03932499369],
                [16880000, 8640000, 0, 320000, -320000, -2636800000000, 452548.3399593904],
                [17200000, 8960000, 6, 240000, 240000, -6278400000000, 339411.2549695428],
                [16960000, 9200000, 0, -320000, 320000, 2483200000000, 452548.3399593904],
                [16640000, 8880000, 0, -30000, 60000, -33600000000, 67082.03932499369],
                [16580000, 8850000, 0, 0, 7150000, -63277500000000, 7150000],
                [9430000, 8850000, 0, 90000, 110000, -1822200000000, 142126.70403551895],
                [9320000, 8940000, 0, 410000, 100000, -4715200000000, 422018.95692018385],
                [9220000, 9350000, 4, 0, 440000, -4114000000000, 440000],
                [8780000, 9350000, 0, -410000, 100000, 2664800000000, 422018.95692018385],
                [8680000, 8940000, 0, -90000, 110000, -202200000000, 142126.70403551895],
                [8570000, 8850000, 0, 0, 7150000, -63277500000000, 7150000],
                [1420000, 8850000, 0, 30000, 60000, -573600000000, 67082.03932499369],
                [1360000, 8880000, 0, 320000, 320000, -3276800000000, 452548.3399593904],
                [1040000, 9200000, 2, -240000, 240000, -1958400000000, 339411.2549695428],
                [800000, 8960000, 0, -320000, -320000, 3123200000000, 452548.3399593904],
                [1120000, 8640000, 0, -60000, -30000, 326400000000, 67082.03932499369],
                [1150000, 8580000, 0, -7160000, 0, 8234000000000, 7160000],
                [1150000, 1420000, 0]
            ],
            lAAMfE: [
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [5, 0, 1, 2, 3, 4, 35],
                    [5],
                    [5], null, null, null, null, [5, 35],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [11, 5, 6, 7, 8, 9, 10],
                    [11],
                    [11], null, null, null, null, [11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11],
                    [11],
                    [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [35, 0, 1, 2, 3, 4, 5],
                    [35, 5], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [5],
                    [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5],
                    [5, 6, 7, 8, 9, 10, 11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [17, 11],
                    [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34],
                    [35, 29], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23],
                    [23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35],
                    [29],
                    [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [29], null, null, null, null, [29],
                    [29],
                    [29, 23, 24, 25, 26, 27, 28], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23, 17], null, null, null, null, [23],
                    [23],
                    [23, 17, 18, 19, 20, 21, 22]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ]
            ]
        };
        iNcCoK[2] = {
            AIONko: 45,
            diBAcc: [
                [1050000, 1050000],
                [16950000, 8950000]
            ],
            PcpKAg: [
                [13130000, 1050000],
                [16950000, 8950000]
            ],
            IPMfPb: [
                [13120000, 5000000],
                [13120000, 3420000]
            ],
            GhfCLm: { _1: [1000000, 1000000], _2: [1000000, 9000000], _3: [9000000, 750000], _4: [9000000, 9250000], _5: [17000000, 1000000], _6: [17000000, 9000000] },
            OMLdpH: { _1: [635000, 635000], _3: [9000000, 390000], _5: [17365000, 635000], _6: [17365000, 9365000], _4: [9000000, 9610000], _2: [635000, 9365000] },
            lLgpbF: [
                [1020000, 1230000, 0, -80000, 30000, 44700000000, 85440.03745317532],
                [990000, 1150000, 0, -280000, 280000, -44800000000, 395979.7974644666],
                [710000, 870000, 1, -160000, -160000, 252800000000, 226274.1699796952],
                [870000, 710000, 0, 280000, -280000, -44800000000, 395979.7974644666],
                [1150000, 990000, 0, 30000, -80000, 44700000000, 85440.03745317532],
                [1230000, 1020000, 0, 0, -7390000, 7537800000000, 7390000],
                [8620000, 1020000, 0, -120000, -140000, 1177200000000, 184390.88914585774],
                [8760000, 900000, 0, -320000, -60000, 2857200000000, 325576.4119219941],
                [8820000, 580000, 3, 0, -360000, 208800000000, 360000],
                [9180000, 580000, 0, 320000, -60000, -2902800000000, 325576.4119219941],
                [9240000, 900000, 0, 120000, -140000, -982800000000, 184390.88914585774],
                [9380000, 1020000, 0, 0, -7390000, 7537800000000, 7390000],
                [16770000, 1020000, 0, -30000, -80000, 584700000000, 85440.03745317532],
                [16850000, 990000, 0, -280000, -280000, 4995200000000, 395979.7974644666],
                [17130000, 710000, 5, 160000, -160000, -2627200000000, 226274.1699796952],
                [17290000, 870000, 0, 280000, 280000, -5084800000000, 395979.7974644666],
                [17010000, 1150000, 0, 80000, 30000, -1395300000000, 85440.03745317532],
                [16980000, 1230000, 0, 7540000, 0, -128029200000000, 7540000],
                [16980000, 8770000, 0, 80000, -30000, -1095300000000, 85440.03745317532],
                [17010000, 8850000, 0, 280000, -280000, -2284800000000, 395979.7974644666],
                [17290000, 9130000, 6, 160000, 160000, -4227200000000, 226274.1699796952],
                [17130000, 9290000, 0, -280000, 280000, 2195200000000, 395979.7974644666],
                [16850000, 9010000, 0, -30000, 80000, -215300000000, 85440.03745317532],
                [16770000, 8980000, 0, 0, 7390000, -66362200000000, 7390000],
                [9380000, 8980000, 0, 120000, 140000, -2382800000000, 184390.88914585774],
                [9240000, 9100000, 0, 320000, 60000, -3502800000000, 325576.4119219941],
                [9180000, 9420000, 4, 0, 360000, -3391200000000, 360000],
                [8820000, 9420000, 0, -320000, 60000, 2257200000000, 325576.4119219941],
                [8760000, 9100000, 0, -120000, 140000, -222800000000, 184390.88914585774],
                [8620000, 8980000, 0, 0, 7390000, -66362200000000, 7390000],
                [1230000, 8980000, 0, 30000, 80000, -755300000000, 85440.03745317532],
                [1150000, 9010000, 0, 280000, 280000, -2844800000000, 395979.7974644666],
                [870000, 9290000, 2, -160000, 160000, -1347200000000, 226274.1699796952],
                [710000, 9130000, 0, -280000, -280000, 2755200000000, 395979.7974644666],
                [990000, 8850000, 0, -80000, -30000, 344700000000, 85440.03745317532],
                [1020000, 8770000, 0, -7540000, 0, 7690800000000, 7540000],
                [1020000, 1230000, 0]
            ],
            lAAMfE: [
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [5, 0, 1, 2, 3, 4, 35],
                    [5],
                    [5], null, null, null, null, [5, 35],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [11, 5, 6, 7, 8, 9, 10],
                    [11],
                    [11], null, null, null, null, [11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11],
                    [11],
                    [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [35, 0, 1, 2, 3, 4, 5],
                    [35, 5], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [5],
                    [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5],
                    [5, 6, 7, 8, 9, 10, 11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [17, 11],
                    [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34],
                    [35, 29], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23],
                    [23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35],
                    [29],
                    [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [29], null, null, null, null, [29],
                    [29],
                    [29, 23, 24, 25, 26, 27, 28], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23, 17], null, null, null, null, [23],
                    [23],
                    [23, 17, 18, 19, 20, 21, 22]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ]
            ]
        };
        iNcCoK[3] = {
            AIONko: 45,
            diBAcc: [
                [1020000, 1020000],
                [16980000, 8980000]
            ],
            PcpKAg: [
                [13130000, 1020000],
                [16980000, 8980000]
            ],
            IPMfPb: [
                [13120000, 5000000],
                [13120000, 3420000]
            ],
            GhfCLm: {},
            OMLdpH: {},
            lLgpbF: [
                [1010000, 1010000, null, 0, -15980000, 16139800000000, 15980000],
                [16990000, 1010000, null, 7980000, 0, -135580200000000, 7980000],
                [16990000, 8990000, null, 0, 15980000, -143660200000000, 15980000],
                [1010000, 8990000, null, -7980000, 0, 8059800000000, 7980000],
                [1010000, 1010000, null]
            ],
            lAAMfE: [
                [
                    [0, 3],
                    [0, 3], null, null, null, null, null, [0, 3],
                    [0, 3], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 3],
                    [0],
                    [0], null, null, null, null, [0, 3],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [0],
                    [0],
                    [0], null, null, null, null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [0],
                    [0],
                    [0], null, null, null, null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [0],
                    [0],
                    [0], null, null, null, null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [0],
                    [0],
                    [0, 1], null, null, null, null, [0],
                    [0],
                    [0, 1], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [0, 1],
                    [0, 1], null, null, null, null, null, [0, 1],
                    [0, 1], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [3, 0],
                    [3, 0], null, null, null, null, null, [3],
                    [3], null, null, null, null, null, [3],
                    [3], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 3],
                    [0],
                    [0], null, null, null, null, [3], null, null, null, null, null, null, [3], null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [0],
                    [0],
                    [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [0],
                    [0],
                    [0, 1], null, null, null, null, null, null, [1], null, null, null, null, null, null, [1], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [1, 0],
                    [1, 0], null, null, null, null, null, [1],
                    [1], null, null, null, null, null, [1],
                    [1], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [3],
                    [3], null, null, null, null, null, [3],
                    [3], null, null, null, null, null, [3, 2],
                    [3, 2], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [3], null, null, null, null, null, null, [3], null, null, null, null, null, null, [2, 3],
                    [2],
                    [2], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, [1], null, null, null, null, null, null, [1], null, null, null, null, [2],
                    [2],
                    [1, 2]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [1],
                    [1], null, null, null, null, null, [1],
                    [1], null, null, null, null, null, [1, 2],
                    [1, 2]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2, 3],
                    [2, 3], null, null, null, null, null, [2, 3],
                    [2, 3], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2, 3],
                    [2],
                    [2], null, null, null, null, [2, 3],
                    [2],
                    [2], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null, null, null, null, [2],
                    [2],
                    [2], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null, null, null, null, [2],
                    [2],
                    [2], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2], null, null, null, null, [2],
                    [2],
                    [2], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2],
                    [2],
                    [2, 1], null, null, null, null, [2],
                    [2],
                    [2, 1]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [1, 2],
                    [1, 2], null, null, null, null, null, [1, 2],
                    [1, 2]
                ]
            ]
        };
        iNcCoK[4] = {
            AIONko: 45,
            diBAcc: [
                [1010000, 2830000],
                [16990000, 7170000]
            ],
            PcpKAg: [
                [5990000, 5490000],
                [12010000, 7170000]
            ],
            IPMfPb: [
                [9000000, 5480000],
                [10190000, 5480000]
            ],
            GhfCLm: { _1: [980000, 980000], _2: [980000, 9020000], _3: [17020000, 980000], _4: [17020000, 9020000] },
            OMLdpH: { _1: [635000, 635000], _3: [17365000, 635000], _4: [17365000, 9365000], _2: [635000, 9365000] },
            lLgpbF: [
                [1000000, 1280000, 0, -70000, 20000, 44400000000, 72801.09889280518],
                [980000, 1210000, 0, -270000, 270000, -62100000000, 381837.66184073564],
                [710000, 940000, 1, -230000, -230000, 379500000000, 325269.11934581184],
                [940000, 710000, 0, 270000, -270000, -62100000000, 381837.66184073564],
                [1210000, 980000, 0, 20000, -70000, 44400000000, 72801.09889280518],
                [1280000, 1000000, 0, 0, -2900000, 2900000000000, 2900000],
                [4180000, 1000000, 0, 1800000, -1800000, -5724000000000, 2545584.412271571],
                [5980000, 2800000, 0, 0, -6040000, 16912000000000, 6040000],
                [12020000, 2800000, 0, -1800000, -1800000, 26676000000000, 2545584.412271571],
                [13820000, 1000000, 0, 0, -2900000, 2900000000000, 2900000],
                [16720000, 1000000, 0, -20000, -70000, 404400000000, 72801.09889280518],
                [16790000, 980000, 0, -270000, -270000, 4797900000000, 381837.66184073564],
                [17060000, 710000, 3, 230000, -230000, -3760500000000, 325269.11934581184],
                [17290000, 940000, 0, 270000, 270000, -4922100000000, 381837.66184073564],
                [17020000, 1210000, 0, 70000, 20000, -1215600000000, 72801.09889280518],
                [17000000, 1280000, 0, 7440000, 0, -126480000000000, 7440000],
                [17000000, 8720000, 0, 70000, -20000, -1015600000000, 72801.09889280518],
                [17020000, 8790000, 0, 270000, -270000, -2222100000000, 381837.66184073564],
                [17290000, 9060000, 4, 230000, 230000, -6060500000000, 325269.11934581184],
                [17060000, 9290000, 0, -270000, 270000, 2097900000000, 381837.66184073564],
                [16790000, 9020000, 0, -20000, 70000, -295600000000, 72801.09889280518],
                [16720000, 9000000, 0, 0, 2900000, -26100000000000, 2900000],
                [13820000, 9000000, 0, -1800000, 1800000, 8676000000000, 2545584.412271571],
                [12020000, 7200000, 0, 0, 6040000, -43488000000000, 6040000],
                [5980000, 7200000, 0, 1800000, 1800000, -23724000000000, 2545584.412271571],
                [4180000, 9000000, 0, 0, 2900000, -26100000000000, 2900000],
                [1280000, 9000000, 0, 20000, 70000, -655600000000, 72801.09889280518],
                [1210000, 9020000, 0, 270000, 270000, -2762100000000, 381837.66184073564],
                [940000, 9290000, 2, -230000, 230000, -1920500000000, 325269.11934581184],
                [710000, 9060000, 0, -270000, -270000, 2637900000000, 381837.66184073564],
                [980000, 8790000, 0, -70000, -20000, 244400000000, 72801.09889280518],
                [1000000, 8720000, 0, -7440000, 0, 7440000000000, 7440000],
                [1000000, 1280000, 0]
            ],
            lAAMfE: [
                [
                    [0, 1, 2, 3, 4, 5, 31],
                    [0, 1, 2, 3, 4, 5, 31, 6], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 31],
                    [0, 1, 2, 3, 4, 5, 31], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [5, 6, 0, 1, 2, 3, 4, 31],
                    [5, 6],
                    [5, 6], null, null, null, null, [5, 6, 31],
                    [5, 6],
                    [5, 6, 7], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [6, 5],
                    [6],
                    [6], null, null, null, null, [6],
                    [6, 7],
                    [6, 7], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [6], null, [8], null, null, null, null, [6, 7],
                    [7],
                    [7, 8], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [8],
                    [8],
                    [8, 9], null, null, null, null, [8, 7],
                    [8, 7],
                    [8], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [8, 9],
                    [8, 9],
                    [8, 9, 10, 11, 12, 13, 14, 15], null, null, null, null, [8, 9, 7],
                    [8, 9],
                    [8, 9, 15], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [9, 10, 11, 12, 13, 14, 15, 8],
                    [9, 10, 11, 12, 13, 14, 15], null, null, null, null, null, [9, 10, 11, 12, 13, 14, 15],
                    [9, 10, 11, 12, 13, 14, 15], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [31, 0, 1, 2, 3, 4, 5],
                    [31, 5, 6], null, null, null, null, null, [31],
                    [31], null, null, null, null, null, [31],
                    [31], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 1, 2, 3, 4, 5, 31],
                    [5, 6],
                    [6], null, null, null, null, [31], null, [6, 7], null, null, null, null, [31], null, [23, 24], null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [6, 7, 5],
                    [6, 7],
                    [6, 7], null, null, null, null, [6, 7],
                    [6, 7],
                    [6, 7], null, null, null, null, [6, 7],
                    [6, 7, 23, 24],
                    [6, 7, 23], null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [7, 6],
                    [7],
                    [7, 8], null, null, null, null, [7, 6],
                    [7],
                    [7, 8], null, null, null, null, [7, 23, 24],
                    [7, 23],
                    [7, 22, 23], null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [7, 8],
                    [7, 8],
                    [7, 8, 9], null, null, null, null, [7, 8],
                    [7, 8],
                    [7, 8], null, null, null, null, [7, 8, 23],
                    [7, 8, 22, 23],
                    [7, 8], null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [8],
                    [8, 9],
                    [9, 10, 11, 12, 13, 14, 15], null, null, null, null, [7, 8], null, [15], null, null, null, null, [22, 23], null, [15], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [15, 8, 9],
                    [15, 9, 10, 11, 12, 13, 14], null, null, null, null, null, [15],
                    [15], null, null, null, null, null, [15],
                    [15], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [31],
                    [31], null, null, null, null, null, [31],
                    [31], null, null, null, null, null, [31, 25, 26, 27, 28, 29, 30],
                    [31, 24, 25], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [31], null, [6, 7], null, null, null, null, [31], null, [23, 24], null, null, null, null, [25, 26, 27, 28, 29, 30, 31],
                    [24, 25],
                    [24], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, [23, 24],
                    [23, 24, 6, 7],
                    [23, 24, 7], null, null, null, null, [23, 24],
                    [23, 24],
                    [23, 24], null, null, null, null, [23, 24, 25],
                    [23, 24],
                    [23, 24], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, [23, 6, 7],
                    [23, 7],
                    [23, 7, 8], null, null, null, null, [23, 24],
                    [23],
                    [23, 22], null, null, null, null, [23, 24],
                    [23],
                    [23, 22], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, [22, 23, 7],
                    [22, 23, 7, 8],
                    [22, 23], null, null, null, null, [22, 23],
                    [22, 23],
                    [22, 23], null, null, null, null, [22, 23],
                    [22, 23],
                    [22, 23, 21], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, [7, 8], null, [15], null, null, null, null, [22, 23], null, [15], null, null, null, null, [22],
                    [21, 22],
                    [15, 16, 17, 18, 19, 20, 21]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [15],
                    [15], null, null, null, null, null, [15],
                    [15], null, null, null, null, null, [15, 21, 22],
                    [15, 16, 17, 18, 19, 20, 21]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [25, 26, 27, 28, 29, 30, 31],
                    [25, 26, 27, 28, 29, 30, 31], null, null, null, null, null, [25, 26, 27, 28, 29, 30, 31],
                    [25, 26, 27, 28, 29, 30, 31, 24], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [24, 25, 31],
                    [24, 25],
                    [24, 25, 23], null, null, null, null, [24, 25, 26, 27, 28, 29, 30, 31],
                    [24, 25],
                    [24, 25], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [24],
                    [24, 23],
                    [24, 23], null, null, null, null, [24, 25],
                    [24],
                    [24], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24],
                    [23],
                    [22, 23], null, null, null, null, [24], null, [22], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [22, 23],
                    [22, 23],
                    [22], null, null, null, null, [22],
                    [22],
                    [22, 21], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [21, 22, 23],
                    [21, 22],
                    [21, 22, 15], null, null, null, null, [21, 22],
                    [21, 22],
                    [21, 22, 15, 16, 17, 18, 19, 20]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [15, 16, 17, 18, 19, 20, 21],
                    [15, 16, 17, 18, 19, 20, 21], null, null, null, null, null, [15, 16, 17, 18, 19, 20, 21, 22],
                    [15, 16, 17, 18, 19, 20, 21]
                ]
            ]
        };
        iNcCoK[5] = {
            AIONko: 45,
            diBAcc: [
                [980000, 980000],
                [17020000, 9020000]
            ],
            PcpKAg: [
                [13130000, 980000],
                [17020000, 9020000]
            ],
            IPMfPb: [
                [13120000, 5000000],
                [13120000, 3420000]
            ],
            GhfCLm: { _1: [970000, 970000], _2: [970000, 9030000], _3: [9000000, 750000], _4: [9000000, 9250000], _5: [17030000, 970000], _6: [17030000, 9030000] },
            OMLdpH: { _1: [620000, 620000], _3: [9000000, 480000], _5: [17380000, 620000], _6: [17380000, 9380000], _4: [9000000, 9520000], _2: [620000, 9380000] },
            lLgpbF: [
                [970000, 1250000, 0, -50000, 10000, 36000000000, 50990.19513592785],
                [960000, 1200000, 0, -280000, 250000, -31200000000, 375366.4875824692],
                [710000, 920000, 1, -210000, -210000, 342300000000, 296984.84809834993],
                [920000, 710000, 0, 250000, -280000, -31200000000, 375366.4875824692],
                [1200000, 960000, 0, 10000, -50000, 36000000000, 50990.19513592785],
                [1250000, 970000, 0, 0, -7380000, 7158600000000, 7380000],
                [8630000, 970000, 0, -30000, -60000, 317100000000, 67082.03932499369],
                [8690000, 940000, 0, -260000, -140000, 2391000000000, 295296.461204668],
                [8830000, 680000, 3, 0, -340000, 231200000000, 340000],
                [9170000, 680000, 0, 260000, -140000, -2289000000000, 295296.461204668],
                [9310000, 940000, 0, 30000, -60000, -222900000000, 67082.03932499369],
                [9370000, 970000, 0, 0, -7380000, 7158600000000, 7380000],
                [16750000, 970000, 0, -10000, -50000, 216000000000, 50990.19513592785],
                [16800000, 960000, 0, -250000, -280000, 4468800000000, 375366.4875824692],
                [17080000, 710000, 5, 210000, -210000, -3437700000000, 296984.84809834993],
                [17290000, 920000, 0, 280000, 250000, -5071200000000, 375366.4875824692],
                [17040000, 1200000, 0, 50000, 10000, -864000000000, 50990.19513592785],
                [17030000, 1250000, 0, 7500000, 0, -127725000000000, 7500000],
                [17030000, 8750000, 0, 50000, -10000, -764000000000, 50990.19513592785],
                [17040000, 8800000, 0, 280000, -250000, -2571200000000, 375366.4875824692],
                [17290000, 9080000, 6, 210000, 210000, -5537700000000, 296984.84809834993],
                [17080000, 9290000, 0, -250000, 280000, 1668800000000, 375366.4875824692],
                [16800000, 9040000, 0, -10000, 50000, -284000000000, 50990.19513592785],
                [16750000, 9030000, 0, 0, 7380000, -66641400000000, 7380000],
                [9370000, 9030000, 0, 30000, 60000, -822900000000, 67082.03932499369],
                [9310000, 9060000, 0, 260000, 140000, -3689000000000, 295296.461204668],
                [9170000, 9320000, 4, 0, 340000, -3168800000000, 340000],
                [8830000, 9320000, 0, -260000, 140000, 991000000000, 295296.461204668],
                [8690000, 9060000, 0, -30000, 60000, -282900000000, 67082.03932499369],
                [8630000, 9030000, 0, 0, 7380000, -66641400000000, 7380000],
                [1250000, 9030000, 0, 10000, 50000, -464000000000, 50990.19513592785],
                [1200000, 9040000, 0, 250000, 280000, -2831200000000, 375366.4875824692],
                [920000, 9290000, 2, -210000, 210000, -1757700000000, 296984.84809834993],
                [710000, 9080000, 0, -280000, -250000, 2468800000000, 375366.4875824692],
                [960000, 8800000, 0, -50000, -10000, 136000000000, 50990.19513592785],
                [970000, 8750000, 0, -7500000, 0, 7275000000000, 7500000],
                [970000, 1250000, 0]
            ],
            lAAMfE: [
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35],
                    [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [5, 0, 1, 2, 3, 4, 35],
                    [5],
                    [5], null, null, null, null, [5, 35],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5],
                    [5],
                    [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [11, 5, 6, 7, 8, 9, 10],
                    [11],
                    [11], null, null, null, null, [11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11],
                    [11],
                    [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [35, 0, 1, 2, 3, 4, 5],
                    [35, 5], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [
                    [0, 1, 2, 3, 4, 5, 35],
                    [5],
                    [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, [5],
                    [5],
                    [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, [5],
                    [5, 6, 7, 8, 9, 10, 11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, [5, 6, 7, 8, 9, 10, 11],
                    [11],
                    [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null
                ],
                [null, null, null, null, [11],
                    [11],
                    [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, [17, 11],
                    [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35],
                    [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34],
                    [35, 29], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23],
                    [23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17],
                    [17], null, null, null, null, null, [17, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35],
                    [29],
                    [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35],
                    [29],
                    [29], null, null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29],
                    [29],
                    [29], null, null, null, null, [29],
                    [29],
                    [29, 23, 24, 25, 26, 27, 28], null, null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29],
                    [23, 24, 25, 26, 27, 28, 29], null, null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29],
                    [23],
                    [23], null
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23],
                    [23],
                    [23, 17], null, null, null, null, [23],
                    [23],
                    [23, 17, 18, 19, 20, 21, 22]
                ],
                [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23],
                    [17, 18, 19, 20, 21, 22, 23]
                ]
            ]
        };
        var dHCPCE, ihDbeD, IJHofk, gFJcBI, jgfLNO, ePDlGD, mfKfpn, NgfpPb;
        var pgOiDk, PlaEDm, NgBOje, mDaMFE, Cignob, oBNGKp;
        var aFmBin, GOCHcG, KkIcel, aOlgBO, FKHFNj;
        var IfpeED, BpAHoj, HGBEdM, LgbFPb, ggOFNa, NFehDM, cGAOBE, NiHkDF, PdOJCJ, ncckdM;
        var gnfGKL, ckOaCH, HpmkkO, hKEiAF, PGDjHJ, McklBp, HiLFPf, ckOECA, DlmjIn, fkHCmP, MhflPF, MOdlNl, EeMCJl;
        var Iipemg, CcDmKl, JgMBLB, MkAkAB, NpJHCM, AFncdg, johhah, OgCIlK, acFOnI, MlfBNK, BPEjBk;
        var aGEjAM = function(GnalKe) {
            var ijmEGj = GnalKe;
            GnalKe.aGEjAM = this;
            this.bIGpib = 0;
            this.cOPbiG = false;
            this.PAFPjb = false;
            this.LOnMIn = true;
            this.nifLGn = true;
            this.ePeklC = 1;
            this.COhpno = function(oNAeLc, emFjKC, gBdoHa) { return ijmEGj.COhpno(oNAeLc, emFjKC, gBdoHa); };
            this.ajgNIF = function() { ijmEGj.ajgNIF(); };
            this.jNfMiL = function(ajJgBK) { ijmEGj.jNfMiL(ajJgBK); };
            this.NBOOaE = function() { ijmEGj.NBOOaE(); };
            this.BCAKgm = function() { ijmEGj.BCAKgm(); };
            this.HjKaLb = function() { ijmEGj.HjKaLb(); };
            this.fpCIhi = function(INfAAc) { ijmEGj.fpCIhi(INfAAc); };
            this.dpneGd = function(JkgjnL) { ijmEGj.dpneGd(JkgjnL); };
            this.ICBiai = function(bekBpl) { ijmEGj.ICBiai(bekBpl); };
            this.OcDfbM = function(GhNgbO) { ijmEGj.OcDfbM(GhNgbO); };
            this.ekPDCM = function(HBeboB) { return ijmEGj.ekPDCM(HBeboB); };
            this.NOfpPB = function(HBeboB) { return ijmEGj.NOfpPB(HBeboB); };
            this.cmfJJm = function(HBeboB) { return ijmEGj.cmfJJm(HBeboB); };
        };
        var hJEkmd = function(MCaldm) { this.OLBcNb(MCaldm); };
        hJEkmd.prototype.OLBcNb = function(MCaldm) {
            if (MCaldm.length < 2) { $error(20819591); return; };
            if (this.JKdCgI) { $error(20819592); return; };
            if (!epCcje(MCaldm[0])) { $error(20819593); return; };
            if (MCaldm[1]) { MeHcPi = 1; } else { MeHcPi = 0; };
            this.aGEjAM = null;
            this.mKjdCO = BLAZE.DPEkhd.amlcmM();
            this.aiIcIi = false;
            this.IOnEGD();
            this.JKdCgI = MCaldm[0];
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
            this.moKlIG = null;
            this.OloiJn = new BLAZE.aajFEA('BilliardsRenderer', BgGFbP[0], BgGFbP[1], 1, MeHcPi);
            this.OloiJn.jICMmC = true;
            this.OloiJn.iKDDhb = false;
            this.OloiJn.gkbHnn = false;
            this.OloiJn.hKPAKA.cncHOL = true;
            this.CdoEBj = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_cue');
            if (!this.CdoEBj) { $error(68377191); return; };
            dLeLMm.dHBnji(this.CdoEBj);
            this.OBIikL = this.CdoEBj.GigegA.container;
            this.GinJoN = this.CdoEBj.GigegA.source;
            this.ngolob = this.CdoEBj.GigegA.anim;
            if (!this.OBIikL || !this.GinJoN || !this.ngolob) { $error(68377192); return; };
            this.oOJDaI = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_table');
            if (!this.oOJDaI) { $error(63950928); return; };
            dLeLMm.dHBnji(this.oOJDaI);
            this.oOJDaI.IgCMNE = true;
            this.KhdkFb = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_effect_foreground');
            if (!this.KhdkFb) { $error(59039921); return; };
            this.kjbKdo = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_effect_background');
            if (!this.kjbKdo) { $error(59683746); return; };
            dLeLMm.dHBnji(this.KhdkFb);
            dLeLMm.dHBnji(this.kjbKdo);
            this.BcoPPH = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_guide');
            if (!this.BcoPPH) { $error(11927504); return; };
            dLeLMm.dHBnji(this.BcoPPH);
            this.eMDgBd = this.BcoPPH.GigegA.start;
            this.oeAcfE = this.BcoPPH.GigegA.start_line;
            this.GFFDda = this.BcoPPH.GigegA.end;
            this.CKigec = this.BcoPPH.GigegA.end_line;
            this.pMmaeL = this.BcoPPH.GigegA.collider;
            this.jHeOOp = this.BcoPPH.GigegA.collider_line;
            this.moKlIG = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_place_ball');
            if (!this.moKlIG) { $error(49862271); return; };
            dLeLMm.dHBnji(this.moKlIG);
            this.moKlIG.jOGpoa = true;
            this.moKlIG.ajJgBK = null;
            this.moKlIG.lBNlFL = false;
            this.moKlIG.classList.remove('deny');
            this.moKlIG.ooLIDD = [0, 0];
            this.DpGKGa = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_spin_menu');
            if (!this.DpGKGa) { $error(94870278); return; };
            dLeLMm.dHBnji(this.DpGKGa);
            var mdKOEp = this;
            this.lNNhGA = function(PfIHKb) { mdKOEp.iJIoEM(PfIHKb); };
            this.IfKgKC = function(PfIHKb) { mdKOEp.mPeMFa(PfIHKb); };
            this.BnGIKH = function(PfIHKb) { mdKOEp.LjKKCk(PfIHKb); };
            this.JlnpAo = function(PfIHKb) { mdKOEp.gnkiop(PfIHKb); };
            this.BOgIMN = function(PfIHKb) { mdKOEp.JOcaDM(PfIHKb); };
            this.MJOLIC = function(PfIHKb) { mdKOEp.MMGKAO(PfIHKb); };
            this.pPLcOn = function(PfIHKb) { mdKOEp.NOEbkC(PfIHKb); };
            this.cIfpkg = function(PfIHKb) { mdKOEp.LhbEgm(PfIHKb); };
            this.EjlNpa = function(PfIHKb) { mdKOEp.dkhnDE(PfIHKb); };
            this.LKeeAA = function(PfIHKb) { mdKOEp.FdePGd(PfIHKb); };
            this.KHGchl = function(PfIHKb) { mdKOEp.iMOKhg(PfIHKb); }
        };
        hJEkmd.prototype.COhpno = function(oNAeLc, emFjKC, gBdoHa) {
            if (!this.JKdCgI) { $warn(2290681); return false; };
            if (this.aiIcIi) { $warn(2290682); return false; };
            if (!oNAeLc) { $warn(2290683); return false; };
            if (!emFjKC) { $warn(2290684); return false; };
            var NHDmDG = 0;
            if (gBdoHa) { NHDmDG = 1; };
            if (MeHcPi != NHDmDG) {
                MeHcPi = NHDmDG;
                this.OloiJn.NOjeil();
                this.OloiJn.nbIBPk();
                this.OloiJn = new BLAZE.aajFEA('BilliardsRenderer', BgGFbP[0], BgGFbP[1], 1, MeHcPi);
                this.OloiJn.jICMmC = true;
                this.OloiJn.iKDDhb = false;
                this.OloiJn.gkbHnn = false;
                this.OloiJn.hKPAKA.cncHOL = true;
            };
            this.IOnEGD();
            if (emFjKC.length != 11) { $warn(64223638); return false; };
            emFjKC[2] = dCibpa(emFjKC[2]);
            emFjKC[3] = dCibpa(emFjKC[3]);
            emFjKC[4] = dCibpa(emFjKC[4]);
            emFjKC[5] = dCibpa(emFjKC[5]);
            emFjKC[6] = dCibpa(emFjKC[6]);
            emFjKC[7] = dCibpa(emFjKC[7]);
            this.oECmEe = emFjKC;
            this.aLhCIk = emFjKC[5] == 1;
            this.dgCCGa = emFjKC[6] == 1;
            this.PANaGB('standard', BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_cue'), this);
            this.kmJAAO = oNAeLc;
            var GigegA = this.kmJAAO.GigegA;
            this.dfOJLM = oNAeLc.parentNode;
            if (!this.dfOJLM) { $error(95882103); return; };
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.hLngmL = GigegA.GameScoreboard;
            this.lpLlFE = GigegA.GameArea;
            this.DLchLC = GigegA.GameFullZone;
            this.lpPabJ = GigegA.GameTable;
            this.oOJDaI.GigegA.table_super_game.classList.remove('AnimSuperGame');
            this.lpPabJ.appendChild(this.oOJDaI);
            this.lpPabJ.appendChild(this.kjbKdo);
            this.OloiJn.IhnhPd(this.lpPabJ);
            this.lpPabJ.appendChild(this.KhdkFb);
            this.lpPabJ.appendChild(this.BcoPPH);
            this.PacccC = dLeLMm.OnKbCc(this.BcoPPH);
            this.moKlIG.ajJgBK = null;
            this.moKlIG.lBNlFL = false;
            this.moKlIG.classList.remove('deny');
            this.moKlIG.ooLIDD = [0, 0];
            this.JKdCgI.aaipCF(BgGFbP, true);
            this.oOJDaI.addEventListener('mousedown', this.lNNhGA, false);
            this.DLchLC.addEventListener('mousedown', this.lNNhGA, false);
            document.addEventListener('mouseup', this.IfKgKC, true);
            document.addEventListener('mousemove', this.BnGIKH, true);
            this.oOJDaI.addEventListener('touchstart', this.JlnpAo, false);
            document.addEventListener('touchend', this.BOgIMN, true);
            document.addEventListener('touchcancel', this.MJOLIC, true);
            document.addEventListener('touchmove', this.pPLcOn, true);
            this.kmJAAO.addEventListener('touchmove', this.cIfpkg, false);
            this.DpGKGa.addEventListener('mouseleave', this.EjlNpa, false);
            this.DpGKGa.addEventListener('mousedown', this.LKeeAA, false);
            this.DpGKGa.addEventListener('touchstart', this.KHGchl, false);
            this.hGcmiD(emFjKC[7], emFjKC[8], emFjKC[9], emFjKC[10], 0);
            this.aiIcIi = true;
            this.mmkIdF(0);
            BLAZE.FEEmCf.egpfPP(this, this.OloiJn);
            return true;
        };
        hJEkmd.prototype.ajgNIF = function() {
            if (!this.JKdCgI) { $warn(59029918); return; };
            BLAZE.FEEmCf.paeaMP();
            this.mmkIdF(0);
            this.CnAILC();
            this.mOCean();
            this.AhpMoN();
            this.IOnEGD();
            this.aiIcIi = false;
            if (this.kmJAAO) { this.kmJAAO.removeEventListener('touchmove', this.cIfpkg, false); };
            if (this.oOJDaI) {
                this.oOJDaI.removeEventListener('mousedown', this.lNNhGA, false);
                this.DLchLC.removeEventListener('mousedown', this.lNNhGA, false);
                document.removeEventListener('mouseup', this.IfKgKC, true);
                document.removeEventListener('mousemove', this.BnGIKH, true);
                this.oOJDaI.removeEventListener('touchstart', this.JlnpAo, false);
                document.removeEventListener('touchend', this.BOgIMN, true);
                document.removeEventListener('touchcancel', this.MJOLIC, true);
                document.removeEventListener('touchmove', this.pPLcOn, true);
                if (this.oOJDaI.parentNode) { this.oOJDaI.parentNode.removeChild(this.oOJDaI); };
                this.oOJDaI.GigegA.table_super_game.classList.remove('AnimSuperGame');
            };
            if (this.DpGKGa) {
                this.DpGKGa.removeEventListener('mouseleave', this.EjlNpa, false);
                this.DpGKGa.removeEventListener('mousedown', this.LKeeAA, false);
                this.DpGKGa.removeEventListener('touchstart', this.KHGchl, false);
            };
            if (this.BcoPPH) { if (this.BcoPPH.parentNode) { this.BcoPPH.parentNode.removeChild(this.BcoPPH); } };
            if (this.KhdkFb) { if (this.KhdkFb.parentNode) { this.KhdkFb.parentNode.removeChild(this.KhdkFb); } };
            if (this.kjbKdo) { if (this.kjbKdo.parentNode) { this.kjbKdo.parentNode.removeChild(this.kjbKdo); } };
            if (this.OloiJn) {
                this.OloiJn.nbIBPk();
                this.OloiJn.aMiNKa();
            };
            if (this.CdoEBj) { if (this.CdoEBj.parentNode) { this.CdoEBj.parentNode.removeChild(this.CdoEBj); } };
            this.kmJAAO = null;
            this.hLngmL = null;
            this.lpLlFE = null;
            this.lpPabJ = null;
        };
        hJEkmd.prototype.HjKaLb = function() {
            this.ajgNIF();
            this.JKdCgI = null;
            this.oOJDaI = null;
            this.BcoPPH = null;
            this.KhdkFb = null;
            this.kjbKdo = null;
            this.OloiJn = null;
            this.moKlIG = null;
            this.DpGKGa = null;
            this.CdoEBj = null;
            this.OBIikL = null;
            this.GinJoN = null;
            oEfbln.cdHKBC(this.ngolob, true);
            this.ngolob = null;
            this.eMDgBd = null;
            this.oeAcfE = null;
            this.GFFDda = null;
            this.CKigec = null;
            this.pMmaeL = null;
            this.jHeOOp = null;
        };
        hJEkmd.prototype.IOnEGD = function() {
            this.nlemFe = null;
            this.jHPcHF = false;
            this.jDPhKk = 0;
            this.GBnioj = '';
            this.oECmEe = null;
            this.aLhCIk = false;
            this.dgCCGa = false;
            this.gaIpJE = [];
            this.ADeOCF = [];
            this.BDKNnM = null;
            this.JekMGJ = null;
            this.cpHPfC = 1.0;
            this.CaKNNK = 0;
            this.MGOIBg = 0;
            this.hOlomK = 0;
            this.cDdhDa = 0;
            this.pJeCBO = 0;
            this.JidbGH = 0;
            this.khbDkm = null;
            this.KJoJHA = null;
            this.oCoAmj = null;
            this.hImPiI = null;
            this.lMPGnH = null;
            this.NKCCjM = 0;
            this.HHCDAK = 0;
            this.oDOoFi = 0;
            this.npEpAb = 0;
            this.GcIhBa = '';
            this.NMOOPN = [0, 0];
            this.kfMiME = [0, 0];
            this.ohKlgh = [0, 0];
            this.CHdncH = 0;
            this.inLdDm = 0;
            this.AEAMlk = eBMKhc;
            this.eDFAeO = 0;
            this.OldbdA = false;
            this.AMkeHI = 0;
            this.noDDJh = 0;
            this.DBJhIi = {};
            this.EgMnOO = [0, 0];
            this.nnDknc = false;
            this.NLoMKI = [0, 0];
            this.jndgcA = -1;
            this.naNdBk = 0;
            this.DICEHA = 0;
            this.fkPBLl = 0;
            this.FDOjAB = 0;
            this.ELlGFH = false;
            this.lNDoji = false;
            this.gLAiKg = null;
            this.JfDElB = false;
            this.kilLED = null;
            this.aPNFBn = null;
            this.aMPfEI = null;
            this.GILDeB = [];
            this.POENJL = [];
            if (this.eMDgBd) { this.eMDgBd.style.display = 'none'; };
            if (this.GFFDda) { this.GFFDda.style.display = 'none'; };
            if (this.pMmaeL) { this.pMmaeL.style.display = 'none'; };
            this.belIOf = -1;
            this.IbEJMc = 0;
            this.AKflnK = 0;
            this.pEcedm = [];
            this.oGAEIn = {};
            this.ccehkL = false;
        };
        hJEkmd.prototype.dpneGd = function(JkgjnL) {
            if (!this.aiIcIi) { return; };
            if (this.oOJDaI) {
                var gNcbKl = this.oOJDaI.GigegA;
                gNcbKl.table_super_game_zp.innerHTML = JkgjnL + ' ZP';
                gNcbKl.table_super_game.classList.add('AnimSuperGame');
            }
        };
        hJEkmd.prototype.OcDfbM = function(bJhmlj) {
            if (!this.aiIcIi) { return; };
            var EjJIlL, iBamkN, GhNgbO;
            this.LDaAFD = dLeLMm.OnKbCc(this.dfOJLM);
            this.PacccC = dLeLMm.OnKbCc(this.BcoPPH);
            var hEdBhi = bJhmlj[0] + 'px';
            var EjbkCN = bJhmlj[1] + 'px';
            this.cpHPfC = bJhmlj[0] / BgGFbP[0];
            if (this.oOJDaI) {
                this.oOJDaI.style.width = hEdBhi;
                this.oOJDaI.style.height = EjbkCN;
                var jLOodg = Math.round(this.JidbGH * this.cpHPfC) + 'px';
                EjJIlL = this.oOJDaI.GigegA.table_markers.style;
                EjJIlL.top = jLOodg;
                EjJIlL.bottom = jLOodg;
                EjJIlL.left = jLOodg;
                EjJIlL.right = jLOodg;
                EjJIlL = this.oOJDaI.GigegA.table_default_fabric.style;
                EjJIlL.top = jLOodg;
                EjJIlL.bottom = jLOodg;
                EjJIlL.left = jLOodg;
                EjJIlL.right = jLOodg;
                EjJIlL = this.oOJDaI.GigegA.table_fabric.style;
                EjJIlL.top = jLOodg;
                EjJIlL.bottom = jLOodg;
                EjJIlL.left = jLOodg;
                EjJIlL.right = jLOodg;
                EjJIlL = this.oOJDaI.GigegA.table_image.style;
                EjJIlL.top = jLOodg;
                EjJIlL.bottom = jLOodg;
                EjJIlL.left = jLOodg;
                EjJIlL.right = jLOodg;
            };
            if (this.OloiJn) {
                this.OloiJn.hKPAKA.style.width = hEdBhi;
                this.OloiJn.hKPAKA.style.height = EjbkCN;
            };
            if (this.moKlIG) { if (this.moKlIG.ajJgBK && this.moKlIG.parentNode && BLAZE.DPEkhd.nJogbk) { this.pdBhgG(this.moKlIG.ajJgBK); } else { this.iFePAm(true, false); } };
            if (this.CdoEBj) {
                GhNgbO = AEOgJp.kDMBPo(JghLjP, this.cpHPfC);
                AEOgJp.cGgNAb(GhNgbO);
                this.OBIikL.style.width = GhNgbO[0] + 'px';
                this.OBIikL.style.height = GhNgbO[1] + 'px';
                this.OBIikL.style.left = (-Math.round(GhNgbO[0] * 0.5)) + 'px';
                if (this.DICEHA > 0) {
                    AEOgJp.MOGook(this.NMOOPN, this.kfMiME);
                    this.NOfpPB(this.kfMiME, this.dfOJLM);
                    AEOgJp.GKEMcP(this.kfMiME, this.LDaAFD);
                    this.CdoEBj.style.left = this.kfMiME[0] + 'px';
                    this.CdoEBj.style.top = this.kfMiME[1] + 'px';
                    this.nnmpEl();
                    if (this.DICEHA == 2) { this.OldbdA = true; }
                };
            };
            if (this.kilLED) { this.oIFHnl(this.kilLED, this.JfDElB); };
            if (this.aPNFBn) { this.LnMCLM(this.aPNFBn); };
            this.FkEDMg();
            this.dNInBK();
            this.DlIMPP();
            BLAZE.FEEmCf.cOmkIC(bJhmlj, this.cpHPfC, this.oDOoFi);
        };
        hJEkmd.prototype.iFePAm = function(EIjfON, FgIOKc) {
            var iBamkN, ilcBeA, EjJIlL = this.moKlIG.style;
            if (EIjfON) {
                var GhNgbO = pOIhMH;
                var FMfbOp = 0;
                if (FgIOKc) { if (BLAZE.DPEkhd.nJogbk) { FMfbOp = faegaG; } } else { if (BLAZE.DPEkhd.nJogbk) { FMfbOp = ChIgGP; } };
                if (FMfbOp < this.cpHPfC) { FMfbOp = this.cpHPfC; };
                GhNgbO = HiMfgN.cGgNAb(GhNgbO * FMfbOp);
                iBamkN = GhNgbO + 'px';
                EjJIlL.width = iBamkN;
                EjJIlL.height = iBamkN;
                iBamkN = HiMfgN.cGgNAb(GhNgbO * -0.5) + 'px';
                EjJIlL.margin = iBamkN + ' 0 0 ' + iBamkN;
            };
            if (!this.moKlIG.ajJgBK) { return; };
            iBamkN = AEOgJp.clhoEK(this.moKlIG.ooLIDD);
            this.ekPDCM(iBamkN);
            if (this.PJIphb(this.moKlIG.ajJgBK[4], this.moKlIG.ajJgBK[1], iBamkN)) {
                if (this.moKlIG.lBNlFL) {
                    this.moKlIG.lBNlFL = false;
                    this.moKlIG.classList.remove('deny');
                }
            } else {
                if (!this.moKlIG.lBNlFL) {
                    this.moKlIG.lBNlFL = true;
                    this.moKlIG.classList.add('deny');
                }
            };
            this.NOfpPB(iBamkN);
            ilcBeA = AEOgJp.GajdDk(iBamkN, this.LDaAFD);
            EjJIlL.left = ilcBeA[0] + 'px';
            EjJIlL.top = ilcBeA[1] + 'px';
        };
        hJEkmd.prototype.eKkChO = function() {
            var ajJgBK = this.moKlIG.ajJgBK;
            if (!ajJgBK) { return; };
            var iBamkN = AEOgJp.clhoEK(this.moKlIG.ooLIDD);
            this.ekPDCM(iBamkN);
            if (!this.PJIphb(ajJgBK[4], ajJgBK[1], iBamkN)) {
                if (BLAZE.DPEkhd.nJogbk) {
                    this.pdBhgG(ajJgBK);
                    this.iFePAm(true, false);
                };
                return;
            };
            this.CnAILC();
            var JBnmFD = this.KkHaGa(ajJgBK[1]);
            if (!JBnmFD) { return; };
            AEOgJp.MOGook(iBamkN, JBnmFD[2]);
            this.AIcGCl(JBnmFD);
            this.OloiJn.jeEAJP();
            this.JKdCgI.pPEGkJ({ c: 'plc', v: [JBnmFD[0], diNKgh.ICGalO(JBnmFD[2][0], 0), diNKgh.ICGalO(JBnmFD[2][1], 0)].join(':') });
            this.idJgpb(ajJgBK[1], ajJgBK[2], ajJgBK[3], false);
        };
        hJEkmd.prototype.noKAMH = function() {
            if (!this.moKlIG.ajJgBK) { return; };
            AEOgJp.MOGook(this.EgMnOO, this.moKlIG.ooLIDD);
            this.iFePAm(true, true);
        };
        hJEkmd.prototype.pdBhgG = function(ajJgBK) {
            if (!ajJgBK) { $warn(57990285); return; };
            ajJgBK[1] = dCibpa(ajJgBK[1]);
            ajJgBK[2] = dCibpa(ajJgBK[2]);
            ajJgBK[3] = dCibpa(ajJgBK[3]);
            ajJgBK[4] = dCibpa(ajJgBK[4]);
            if (this.moKlIG.lBNlFL) {
                this.moKlIG.lBNlFL = false;
                this.moKlIG.classList.remove('deny');
            };
            this.moKlIG.ajJgBK = ajJgBK;
            this.dfOJLM.appendChild(this.moKlIG);
            if (BLAZE.DPEkhd.nJogbk) {
                var JBnmFD = this.KkHaGa(ajJgBK[1]);
                if (JBnmFD) {
                    AEOgJp.MOGook(JBnmFD[2], this.moKlIG.ooLIDD);
                    this.NOfpPB(this.moKlIG.ooLIDD);
                }
            } else { AEOgJp.MOGook(this.EgMnOO, this.moKlIG.ooLIDD); };
            this.iFePAm(false, false);
        };
        hJEkmd.prototype.CnAILC = function() {
            if (this.moKlIG) {
                if (this.moKlIG.ajJgBK || this.moKlIG.parentNode) {
                    this.iFePAm(true, false);
                    this.moKlIG.ajJgBK = null;
                    this.moKlIG.lBNlFL = false;
                    this.moKlIG.classList.remove('deny');
                    if (this.moKlIG.parentNode) { this.moKlIG.parentNode.removeChild(this.moKlIG); }
                };
            }
        };
        hJEkmd.prototype.PJIphb = function(BcPafn, EFpEJB, ooLIDD) {
            if (BcPafn == 2) {
                jIbNPl.lKpajk(this.khbDkm.hGehBG, ooLIDD);
                IJHofk = this.khbDkm.EMlFPp[0];
                gFJcBI = this.khbDkm.EMlFPp[1];
                if (IJHofk[0] == gFJcBI[0]) { if (ooLIDD[0] < IJHofk[0]) { ooLIDD[0] = IJHofk[0]; } } else { if (ooLIDD[1] < IJHofk[1]) { ooLIDD[1] = IJHofk[1]; } };
                var mDgBid = AEOgJp.IAiaok(IJHofk, ooLIDD);
                if (mDgBid > this.khbDkm.EMlFPp[2]) {
                    var dMiOKI = AEOgJp.GajdDk(ooLIDD, IJHofk);
                    AEOgJp.JIHKfG(dMiOKI);
                    AEOgJp.obdCcB(dMiOKI, this.khbDkm.EMlFPp[2] - MLBlFB);
                    dMiOKI = AEOgJp.olNCjJ(IJHofk, dMiOKI);
                    AEOgJp.cGgNAb(dMiOKI);
                    AEOgJp.MOGook(dMiOKI, ooLIDD);
                }
            } else if (BcPafn == 1) { jIbNPl.lKpajk(this.khbDkm.cPmHPL, ooLIDD); } else { jIbNPl.lKpajk(this.khbDkm.hGehBG, ooLIDD); };
            var GPHCpN = this.oDOoFi + PEiBck;
            var cJcdCM, DpfEAC = this.pEcedm.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { pgOiDk = this.pEcedm[cJcdCM]; if (pgOiDk[0] != EFpEJB) { if (pgOiDk[1]) { if (AEOgJp.IAiaok(ooLIDD, pgOiDk[2]) < GPHCpN) { return false; } }; } };
            return true;
        };
        hJEkmd.prototype.jNfMiL = function(ajJgBK) {
            if (!ajJgBK) { return; };
            this.jHPcHF = false;
            this.nlemFe = ajJgBK;
            this.nlemFe.OcMDpE = 0;
            window.setTimeout(this.bIdfjh, 500, this);
        };
        hJEkmd.prototype.NBOOaE = function() {
            if (!this.nlemFe) { return; };
            this.JKdCgI.aFDeff();
            this.jHPcHF = false;
            this.nlemFe.OcMDpE = 0;
            this.pDhCiA();
        };
        hJEkmd.prototype.GilbBF = function() {
            if (!this.nlemFe) { return; };
            if (this.nlemFe.OcMDpE >= this.nlemFe.bKgEdk.length - 1) { return; };
            this.jHPcHF = true;
            this.JKdCgI.jfBhKJ();
            this.JKdCgI.aFOEfh();
            this.JKdCgI.OEOpEB();
        };
        hJEkmd.prototype.BCAKgm = function() {
            if (!this.nlemFe) { return; };
            this.jHPcHF = false;
            this.JKdCgI.BBFIek();
            if (!this.ccehkL && !this.lNDoji) { this.pDhCiA(); }
        };
        hJEkmd.prototype.bIdfjh = function(fkiijB) {
            if (!fkiijB.nlemFe || !fkiijB.aiIcIi) { return; };
            fkiijB.pDhCiA();
        };
        hJEkmd.prototype.pDhCiA = function() {
            if (!this.aiIcIi) { return; };
            var iBamkN, EjJIlL, ajJgBK, bBOchF;
            var EmNmnC = false;
            if (this.gaIpJE.length > 0) {
                ajJgBK = this.gaIpJE.shift();
                bBOchF = ajJgBK[0];
                if (bBOchF != 'q') {
                    this.mmkIdF(0);
                    this.CnAILC();
                };
                if (bBOchF == 'i') {
                    this.GBnioj = ajJgBK[1];
                    this.NdfECE(this.GBnioj);
                    this.JKdCgI.cBIfjo();
                    this.AhpMoN();
                    EmNmnC = true;
                } else if (bBOchF == 'z') { this.IGOEpd(); } else if (bBOchF == 's') {
                    ajJgBK.shift();
                    this.GAmlpF(ajJgBK);
                } else if (bBOchF == 'a') { this.idJgpb(dCibpa(ajJgBK[1]), dCibpa(ajJgBK[2]), dCibpa(ajJgBK[3]), false); } else if (bBOchF == 'b') { this.pdBhgG(ajJgBK); } else if (bBOchF == 'c') { this.dgcBkM(ajJgBK); } else if (bBOchF == 'r') { this.idJgpb(dCibpa(ajJgBK[1]), dCibpa(ajJgBK[2]), 0, true); } else if (bBOchF == 'u') {
                    iBamkN = dCibpa(ajJgBK[1]);
                    var JBnmFD = this.KkHaGa(iBamkN);
                    if (JBnmFD) {
                        var NgBOje = JBnmFD[6];
                        var mDaMFE = JBnmFD[7];
                        JBnmFD[1] = 1;
                        NgBOje.hIgAJC = [1, 1];
                        NgBOje.GNDJnF = 1;
                        mDaMFE.GNDJnF = 1;
                        JBnmFD[3][0] = 0;
                        JBnmFD[3][1] = 0;
                        JBnmFD[5] = 0;
                        if (JBnmFD[8]) { JBnmFD[8].GNDJnF = 1; };
                        JBnmFD[9] = 0;
                        JBnmFD[10] = 0;
                        JBnmFD[11] = null;
                        pgOiDk[2][0] = diNKgh.edFiCc(ajJgBK[3]);
                        pgOiDk[2][1] = diNKgh.edFiCc(ajJgBK[4]);
                        this.AIcGCl(pgOiDk);
                        this.OloiJn.jeEAJP();
                    };
                    this.idJgpb(iBamkN, dCibpa(ajJgBK[2]), 0, true);
                } else if (bBOchF == 'q') {
                    if (this.DICEHA == 2) {
                        this.noDDJh = HiMfgN.pPiioc(HiMfgN.jnJjhC(dCibpa(ajJgBK[1]) * 0.1));
                        this.OldbdA = true;
                    }
                } else if (bBOchF == 'p') { this.HeDJeM(dCibpa(ajJgBK[1]), [dCibpa(ajJgBK[4]), dCibpa(ajJgBK[5])], [dCibpa(ajJgBK[6]), dCibpa(ajJgBK[7]), dCibpa(ajJgBK[8])], dCibpa(ajJgBK[2]), dCibpa(ajJgBK[3]), 2); } else if (bBOchF == 'n') {
                    iBamkN = null;
                    if (ajJgBK[3] != '') { iBamkN = ajJgBK[3].split(';'); };
                    EjJIlL = null;
                    if (ajJgBK[4] != '') { EjJIlL = ajJgBK[4].split(';'); };
                    this.aHGMFN(dCibpa(ajJgBK[1]), dCibpa(ajJgBK[2]), iBamkN, EjJIlL);
                } else { $warn('GC ' + bBOchF); }
            };
            if (this.ADeOCF.length > 0 && !EmNmnC) {
                this.JKdCgI.aFDeff();
                var ePoLdm = this.ADeOCF.shift();
                var NlPIck = HiMfgN.dcahnC(MmFnAP() - ePoLdm[0]);
                ajJgBK = ePoLdm[1];
                var cIhEIM = ajJgBK.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    iBamkN = ajJgBK[cJcdCM].split('#');
                    bBOchF = iBamkN[0];
                    if (bBOchF == 'p') { if (iBamkN.length < 4) { this.JKdCgI.HhlhKD(iBamkN[1], IpFeae('computer_player'), iBamkN[3]); } else { this.JKdCgI.HhlhKD(iBamkN[1], iBamkN[2], iBamkN[3]); } } else if (bBOchF == 's') { this.JKdCgI.AKlbbJ(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'i') { this.JKdCgI.laipPe(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'h') { this.JKdCgI.Fgbpjh(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'j') { this.JKdCgI.peaOmi(iBamkN[1], iBamkN[2]); } else if (bBOchF == 'c') { this.JKdCgI.PHafCn(iBamkN[1]); } else if (bBOchF == 't') { this.JKdCgI.abgdOj(dCibpa(iBamkN[1]) + NlPIck, iBamkN[2]); } else if (bBOchF == 'e') { this.JKdCgI.iClGgO(iBamkN[1]); } else if (bBOchF == 'r') { this.JKdCgI.FkCIHc(iBamkN[1], dCibpa(iBamkN[2]) + NlPIck); } else if (bBOchF == 'w') {
                        this.JKdCgI.OEOpEB();
                        this.mmkIdF(0);
                        this.CnAILC();
                        this.JKdCgI.JAdFJk(iBamkN[1], iBamkN[2], iBamkN[3], iBamkN[4], iBamkN[5], iBamkN[6]);
                    } else if (bBOchF == 'b') { if (iBamkN.length < 2) { this.oIFHnl(null, false); } else { this.oIFHnl(iBamkN[1].split(';'), false); } } else if (bBOchF == 'k') { this.LnMCLM(iBamkN[1].split(';')); } else if (bBOchF == 'o') { this.AhpMoN(); } else if (bBOchF == 'v') { this.JKdCgI.fNCPnN(); var eDLbgB = iBamkN.length; for (var EnibFl = 1; EnibFl < eDLbgB; EnibFl++) { this.JKdCgI.nabEiA(iBamkN[EnibFl]); } } else if (bBOchF == 'l') { this.JKdCgI.nabEiA(iBamkN[1]); } else { $warn('IC ' + bBOchF); }
                };
            };
            if (this.gaIpJE.length > 0 || this.ADeOCF.length > 0) { this.pDhCiA(); } else if (this.nlemFe) {
                if (!this.ccehkL && !this.lNDoji && !this.jHPcHF) {
                    var OcMDpE = this.nlemFe.OcMDpE;
                    var bKgEdk = this.nlemFe.bKgEdk;
                    if (OcMDpE < bKgEdk.length) {
                        var PfIHKb = bKgEdk[OcMDpE];
                        OcMDpE = OcMDpE + 1;
                        this.nlemFe.OcMDpE = OcMDpE;
                        this.fpCIhi(PfIHKb);
                    } else { this.JKdCgI.BBFIek(); }
                };
            }
        };
        hJEkmd.prototype.fpCIhi = function(INfAAc) {
            if (!this.aiIcIi) { return; };
            if (!INfAAc) { return; };
            if (INfAAc.hasOwnProperty('gcn')) { this.JKdCgI.dFbJkH(); };
            if (INfAAc.hasOwnProperty('cpi')) { this.aGEjAM.bIGpib = dCibpa(INfAAc['cpi']); };
            var gFiOmG = false;
            if (INfAAc.hasOwnProperty('gv')) {
                gFiOmG = true;
                var khFnEl = String(INfAAc.gv).split('|');
                var cIhEIM = khFnEl.length;
                for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) {
                    var IDKdaa = khFnEl[cJcdCM].split('#');
                    var EEkoKP = IDKdaa[0];
                    if (EEkoKP == 'z' || EEkoKP == 's') {
                        var hmDdiL = null;
                        var PPcNFa = this.gaIpJE.length;
                        if (PPcNFa > 0) { PPcNFa--; if (this.gaIpJE[PPcNFa][0] == 'i') { hmDdiL = this.gaIpJE[PPcNFa]; } };
                        this.gaIpJE = [IDKdaa];
                        if (hmDdiL) { this.gaIpJE.unshift(hmDdiL); }
                    } else { this.gaIpJE.push(IDKdaa); }
                };
            };
            if (INfAAc.hasOwnProperty('gs')) {
                gFiOmG = true;
                this.ADeOCF.push([MmFnAP(), String(INfAAc.gs).split('|')]);
            };
            if (!this.ccehkL && gFiOmG) { this.pDhCiA(); }
        };
        hJEkmd.prototype.ICBiai = function(bekBpl) {
            if (!this.aiIcIi) { return; };
            if (this.naNdBk > 0) { this.naNdBk = 0; };
            if (this.ccehkL) { this.aeCfaO(); } else if (this.DICEHA == 1) {
                this.eDFAeO = AEOgJp.EfhfDe(this.kfMiME, this.ohKlgh);
                dLeLMm.MHlIiE(this.CdoEBj, this.eDFAeO);
                this.KeOhIo();
                if (this.ELlGFH) {
                    this.CHdncH = this.CHdncH + (this.AEAMlk * BLAZE.afEDBA.ddnjdC);
                    if (this.CHdncH > 1) {
                        this.CHdncH = 1;
                        this.AEAMlk = -this.AEAMlk;
                    } else if (this.CHdncH <= 0) {
                        this.CHdncH = 0;
                        this.AEAMlk = -this.AEAMlk;
                    };
                    this.nnmpEl();
                }
            } else if (this.DICEHA == 2) {
                if (this.OldbdA) {
                    aFmBin = this.noDDJh;
                    if (this.lpPabJ.fhhfhh) { aFmBin = HiMfgN.bdGDjo(aFmBin + HiMfgN.ggiaCo); };
                    IfpeED = HiMfgN.bdGDjo(aFmBin - this.AMkeHI);
                    if (Math.abs(IfpeED) < hLGAig) {
                        this.OldbdA = false;
                        this.AMkeHI = aFmBin;
                    } else {
                        IfpeED = IfpeED * 0.1;
                        if (IfpeED > 0) { if (IfpeED < hLGAig) { IfpeED = hLGAig; } } else { if (IfpeED > -hLGAig) { IfpeED = -hLGAig; } };
                        this.AMkeHI = HiMfgN.bdGDjo(this.AMkeHI + IfpeED);
                    };
                    dLeLMm.MHlIiE(this.CdoEBj, this.AMkeHI);
                }
            };
            if (BLAZE.FEEmCf.iFcCgl(bekBpl)) { if (!this.ccehkL) { this.OloiJn.jeEAJP(); } };
        };
        hJEkmd.prototype.HgKPAI = function() { if (this.aLhCIk && this.aGEjAM.LOnMIn) { return true; }; return false; };
        hJEkmd.prototype.FkEDMg = function() {
            if (!this.nlfGAj) { return; };
            this.eMDgBd.style.display = 'none';
            this.GFFDda.style.display = 'none';
            this.pMmaeL.style.display = 'none';
            this.nlfGAj = false;
        };






        // here
        hJEkmd.prototype.MJpbeh = function() {
            var PHdjDc = 0;
            if (this.HgKPAI()) {
                PHdjDc = 2;
                if (this.aGEjAM.nifLGn) { PHdjDc = 3; }
            } else if (BLAZE.DPEkhd.nJogbk && this.aGEjAM.LOnMIn) {
                PHdjDc = 1;
            };
            if (PHdjDc == 0) {
                if (this.nlfGAj) {
                    PHdjDc = 3;
                    this.FkEDMg();
                };

            };
            IJHofk = AEOgJp.clhoEK(this.NMOOPN);
            gFJcBI = AEOgJp.clhoEK(this.EgMnOO);
            this.ekPDCM(gFJcBI);
            acFOnI = AEOgJp.GajdDk(gFJcBI, IJHofk);
            aFmBin = HiMfgN.cGgNAb(AEOgJp.FkDjcj(acFOnI) / MLBlFB * this.cpHPfC);
            AEOgJp.JIHKfG(acFOnI);
            if (BLAZE.DPEkhd.nJogbk) {
                gFJcBI = AEOgJp.kDMBPo(acFOnI, 20000000);
                AEOgJp.pjMFnl(gFJcBI, IJHofk);
            };
            NiHkDF = [0];
            if (PHdjDc == 1) { mfKfpn = true; } else {
                cGAOBE = AEOgJp.IAiaok(IJHofk, gFJcBI);
                jgfLNO = this.hImPiI.length - 1;
                for (ePDlGD = 0; ePDlGD < jgfLNO; ePDlGD++) {
                    ncckdM = this.jKLPCa(IJHofk, gFJcBI, this.hImPiI[ePDlGD], this.hImPiI[ePDlGD + 1]);
                    if (ncckdM) {
                        NpJHCM = AEOgJp.IAiaok(IJHofk, ncckdM);
                        if (NpJHCM < 0) { NpJHCM = 0; };
                        if (cGAOBE > NpJHCM) {
                            cGAOBE = NpJHCM;
                            NiHkDF[0] = 1;
                            NiHkDF[1] = this.hImPiI[ePDlGD];
                            NiHkDF[2] = this.hImPiI[ePDlGD + 1];
                            NiHkDF[3] = NpJHCM;
                            NiHkDF[4] = ncckdM;
                            NiHkDF[5] = ePDlGD;
                        }
                    };
                };
                if (PHdjDc == 3) {
                    var JBnmFD = this.KkHaGa(this.npEpAb);
                    Cignob = JBnmFD[2];
                    LgbFPb = cGAOBE;
                    oBNGKp = AEOgJp.kDMBPo(acFOnI, LgbFPb);
                    ggOFNa = AEOgJp.olNCjJ(Cignob, oBNGKp);
                    GOCHcG = this.pEcedm;
                    BpAHoj = GOCHcG.length;
                    for (IfpeED = 0; IfpeED < BpAHoj; IfpeED++) {
                        KkIcel = GOCHcG[IfpeED];
                        if (KkIcel[1]) {
                            if (KkIcel[0] != this.npEpAb) {
                                HGBEdM = this.dKhlAk(cGAOBE, Cignob, ggOFNa, oBNGKp, LgbFPb, KkIcel[2], KkIcel[3]);
                                if (HGBEdM) {
                                    cGAOBE = HGBEdM[0];
                                    NiHkDF[0] = 2;
                                    NiHkDF[1] = HGBEdM;
                                    NiHkDF[2] = KkIcel;
                                }
                            };
                        }
                    };
                };
                mfKfpn = true;
                if (NiHkDF[0] == 2) {
                    HGBEdM = NiHkDF[1];
                    gFJcBI = AEOgJp.clhoEK(HGBEdM[1]);
                    acFOnI = AEOgJp.GajdDk(gFJcBI, IJHofk);
                    aFmBin = HiMfgN.cGgNAb(AEOgJp.FkDjcj(acFOnI) / MLBlFB * this.cpHPfC);
                    AEOgJp.JIHKfG(acFOnI);
                    AEOgJp.obdCcB(acFOnI, MLBlFB);
                    mfKfpn = false;
                    NgfpPb = this.eMDgBd.style;
                    NgfpPb.display = '';
                    this.cmfJJm(IJHofk);
                    AEOgJp.GKEMcP(IJHofk, this.PacccC);
                    AEOgJp.cGgNAb(IJHofk);
                    NgfpPb.left = IJHofk[0] + 'px';
                    NgfpPb.top = IJHofk[1] + 'px';
                    this.oeAcfE.style.width = aFmBin + 'px';
                    dLeLMm.MHlIiE(this.eMDgBd, AEOgJp.dNELFd(acFOnI));
                    NgfpPb = this.GFFDda.style;
                    NgfpPb.display = '';
                    this.cmfJJm(gFJcBI);
                    AEOgJp.GKEMcP(gFJcBI, this.PacccC);
                    AEOgJp.cGgNAb(gFJcBI);
                    NgfpPb.left = gFJcBI[0] + 'px';
                    NgfpPb.top = gFJcBI[1] + 'px';
                    OgCIlK = HGBEdM[2];
                    MlfBNK = HiMfgN.cGgNAb(AEOgJp.FkDjcj(OgCIlK));
                    this.CKigec.style.width = 1000 + 'px';
                    dLeLMm.MHlIiE(this.GFFDda, AEOgJp.dNELFd(OgCIlK));
                    NgfpPb = this.pMmaeL.style;
                    NgfpPb.display = '';
                    KkIcel = NiHkDF[2];
                    gFJcBI = AEOgJp.clhoEK(KkIcel[2]);
                    this.cmfJJm(gFJcBI);
                    AEOgJp.GKEMcP(gFJcBI, this.PacccC);
                    AEOgJp.cGgNAb(gFJcBI);
                    NgfpPb.left = gFJcBI[0] + 'px';
                    NgfpPb.top = gFJcBI[1] + 'px';
                    OgCIlK = HGBEdM[3];
                    MlfBNK = HiMfgN.cGgNAb(AEOgJp.FkDjcj(OgCIlK));
                    this.jHeOOp.style.width = 1000 + 'px';
                    dLeLMm.MHlIiE(this.pMmaeL, AEOgJp.dNELFd(OgCIlK));
                } else if (NiHkDF[0] > 0) {
                    this.pMmaeL.style.display = 'none';
                    gFJcBI = NiHkDF[4];
                    if (NiHkDF[1][2] == 0 || NiHkDF[1][2] == null) {
                        acFOnI = AEOgJp.GajdDk(gFJcBI, IJHofk);
                        aFmBin = HiMfgN.cGgNAb(AEOgJp.FkDjcj(acFOnI) / MLBlFB * this.cpHPfC);
                        AEOgJp.JIHKfG(acFOnI);
                        AEOgJp.obdCcB(acFOnI, MLBlFB);
                        OgCIlK = this.KnbifO(acFOnI, NiHkDF[1], NiHkDF[2]);
                        johhah = AEOgJp.kDMBPo(OgCIlK, FibKcf[0] * 2);
                        AEOgJp.pjMFnl(johhah, gFJcBI);
                        NgfpPb = NiHkDF[5];
                        cGAOBE = 99999999;
                        PdOJCJ = null;
                        for (ePDlGD = 0; ePDlGD < jgfLNO; ePDlGD++) {
                            if (ePDlGD != NgfpPb) {
                                ncckdM = this.jKLPCa(gFJcBI, johhah, this.hImPiI[ePDlGD], this.hImPiI[ePDlGD + 1]);
                                if (ncckdM) {
                                    NpJHCM = AEOgJp.IAiaok(gFJcBI, ncckdM);
                                    if (NpJHCM < 0) { NpJHCM = 0; };
                                    if (cGAOBE > NpJHCM) {
                                        cGAOBE = NpJHCM;
                                        PdOJCJ = ncckdM;
                                    }
                                };
                            }
                        };
                        if (PdOJCJ) {
                            mfKfpn = false;
                            NgfpPb = this.eMDgBd.style;
                            NgfpPb.display = '';
                            this.cmfJJm(IJHofk);
                            AEOgJp.GKEMcP(IJHofk, this.PacccC);
                            AEOgJp.cGgNAb(IJHofk);
                            NgfpPb.left = IJHofk[0] + 'px';
                            NgfpPb.top = IJHofk[1] + 'px';
                            this.oeAcfE.style.width = aFmBin + 'px';
                            dLeLMm.MHlIiE(this.eMDgBd, AEOgJp.dNELFd(acFOnI));
                            NgfpPb = this.GFFDda.style;
                            NgfpPb.display = '';
                            this.cmfJJm(gFJcBI);
                            AEOgJp.GKEMcP(gFJcBI, this.PacccC);
                            AEOgJp.cGgNAb(gFJcBI);
                            NgfpPb.left = gFJcBI[0] + 'px';
                            NgfpPb.top = gFJcBI[1] + 'px';
                            this.CKigec.style.width = HiMfgN.cGgNAb(cGAOBE / MLBlFB * this.cpHPfC) + 'px';
                            dLeLMm.MHlIiE(this.GFFDda, AEOgJp.dNELFd(OgCIlK));
                        }
                    };
                }
            };
            if (mfKfpn) {
                this.GFFDda.style.display = 'none';
                this.pMmaeL.style.display = 'none';
                AEOgJp.obdCcB(acFOnI, MLBlFB);
                NgfpPb = this.eMDgBd.style;
                NgfpPb.display = '';
                this.cmfJJm(IJHofk);
                AEOgJp.GKEMcP(IJHofk, this.PacccC);
                AEOgJp.cGgNAb(IJHofk);
                NgfpPb.left = IJHofk[0] + 'px';
                NgfpPb.top = IJHofk[1] + 'px';
                this.oeAcfE.style.width = aFmBin + 'px';
                dLeLMm.MHlIiE(this.eMDgBd, AEOgJp.dNELFd(acFOnI));
            };
            this.nlfGAj = true;
        };










        hJEkmd.prototype.idJgpb = function(fIdnmf, gHFhPn, iCnNOm, dNFffp) {
            if (!this.aiIcIi) { return; };
            if (!this.CdoEBj) { return; };
            if (!this.CdoEBj.parentNode) { this.dfOJLM.appendChild(this.CdoEBj); };
            if (iCnNOm >= 0) { BLAZE.FEEmCf.JofPmN(iCnNOm); };
            this.fkPBLl = 0;
            this.FDOjAB = -1;
            this.lNDoji = false;
            this.ccehkL = false;
            this.ELlGFH = false;
            fIdnmf = dCibpa(fIdnmf);
            pgOiDk = this.KkHaGa(fIdnmf);
            if (!pgOiDk) { return; };
            if (!pgOiDk[1]) { return; };
            this.npEpAb = fIdnmf;
            this.OBIikL.style.top = HiMfgN.cGgNAb(this.cpHPfC * ekJaln) + 'px';
            this.CHdncH = 0;
            this.AEAMlk = eBMKhc;
            this.NMOOPN = AEOgJp.clhoEK(pgOiDk[2]);
            AEOgJp.MOGook(this.NMOOPN, this.kfMiME);
            this.NOfpPB(this.kfMiME, this.dfOJLM);
            AEOgJp.GKEMcP(this.kfMiME, this.LDaAFD);
            this.CdoEBj.style.left = this.kfMiME[0] + 'px';
            this.CdoEBj.style.top = this.kfMiME[1] + 'px';
            if (dNFffp) { this.DICEHA = 2; } else {
                this.DICEHA = 1;
                this.fkPBLl = MmFnAP();
                this.CmmiDb();
                this.fhGCdL();
                this.oIpoLH();
                this.MJpbeh();
            };
            this.AMkeHI = AEOgJp.EfhfDe(this.kfMiME, this.ohKlgh);
            dLeLMm.MHlIiE(this.CdoEBj, this.AMkeHI);
            gHFhPn = dCibpa(gHFhPn);
            if (gHFhPn >= 0) {
                var EgicPo = '';
                var OKgKcn, dFNaNi;
                if (gHFhPn < 100) { OKgKcn = 'cue' + gHFhPn; } else if (gHFhPn < 1000) {
                    gHFhPn -= 100;
                    OKgKcn = 'pcue' + (gHFhPn);
                } else {
                    gHFhPn -= 1000;
                    OKgKcn = 'acue' + (gHFhPn);
                };
                if (this.GcIhBa == OKgKcn) {
                    if (OKgKcn.substring(0, 4) == 'acue') {
                        this.GinJoN.classList.add('sprite');
                        dFNaNi = cmkjdC[gHFhPn];
                        this.ngolob.style.top = dFNaNi[0] + '%';
                        this.ngolob.style.bottom = (100 - dFNaNi[0] - 50) + '%';
                        oEfbln.FglKol(this.ngolob, dFNaNi[3], dFNaNi[1], dFNaNi[2]);
                    }
                } else {
                    var oPfCPF = false;
                    if (gHFhPn == 0) { EgicPo = this.DBJhIi.standard; } else {
                        this.GcIhBa = '';
                        if (this.DBJhIi[OKgKcn]) { EgicPo = this.DBJhIi[OKgKcn]; } else {
                            BLAZE.DPEkhd.heEBin(OKgKcn, aaPJke + OKgKcn + '.png?' + BLAZE.CONTENT_VERSION, 1, this.PANaGB, this);
                            if (this.DBJhIi[OKgKcn]) { EgicPo = this.DBJhIi[OKgKcn]; } else {
                                EgicPo = this.DBJhIi.standard;
                                oPfCPF = true;
                            }
                        };
                    };
                    this.GcIhBa = OKgKcn;
                    this.GinJoN.style.backgroundImage = EgicPo;
                    if (OKgKcn.substring(0, 4) == 'acue' && !oPfCPF) {
                        this.GinJoN.classList.add('sprite');
                        this.ngolob.style.backgroundImage = EgicPo;
                        dFNaNi = cmkjdC[gHFhPn];
                        this.ngolob.style.top = dFNaNi[0] + '%';
                        this.ngolob.style.bottom = (100 - dFNaNi[0] - 50) + '%';
                        oEfbln.FglKol(this.ngolob, dFNaNi[3], dFNaNi[1], dFNaNi[2]);
                    } else {
                        this.GinJoN.classList.remove('sprite');
                        this.ngolob.style.backgroundImage = '';
                        oEfbln.cdHKBC(this.ngolob, true);
                    }
                };
            }
        };
        hJEkmd.prototype.mmkIdF = function(JamHJL) {
            if (!this.aiIcIi) { return; };
            this.iMaEeD();
            this.HDLfgG();
            this.FkEDMg();
            this.DICEHA = 0;
            this.fkPBLl = 0;
            this.FDOjAB = -1;
            this.ELlGFH = false;
            if (!this.CdoEBj) { return; };
            if (this.CdoEBj.parentNode) {
                JamHJL = dCibpa(JamHJL);
                if (JamHJL > 0) { window.setTimeout(this.HAGcEA, JamHJL, this); } else {
                    oEfbln.cdHKBC(this.ngolob, true);
                    this.CdoEBj.parentNode.removeChild(this.CdoEBj);
                }
            };
        };
        hJEkmd.prototype.HAGcEA = function(fkiijB) {
            if (fkiijB) {
                if (fkiijB.CdoEBj.parentNode && fkiijB.DICEHA == 0) {
                    oEfbln.cdHKBC(fkiijB.ngolob, true);
                    fkiijB.CdoEBj.parentNode.removeChild(fkiijB.CdoEBj);
                }
            };
        };
        hJEkmd.prototype.KeOhIo = function(jhjjJO) {
            if (this.DICEHA != 1 || !this.aGEjAM.cOPbiG) { return; };
            var iBamkN = HiMfgN.cGgNAb(HiMfgN.jnJjhC(HiMfgN.BpmoDa(this.eDFAeO)) * 10);
            if (Math.abs(this.FDOjAB - iBamkN) < 20) { return; };
            var NOPEcM = BLAZE.afEDBA.ACLAFc;
            if (NOPEcM - this.fkPBLl > lEaKoD) {
                this.fkPBLl = NOPEcM;
                this.FDOjAB = iBamkN;
                this.JKdCgI.pPEGkJ({ c: 'q', v: iBamkN });
            }
        };
        hJEkmd.prototype.nnmpEl = function() {
            if (!this.CdoEBj) { return; };
            this.OBIikL.style.top = HiMfgN.cGgNAb(this.cpHPfC * (ekJaln + (this.CHdncH * bDeDeB))) + 'px';
        };
        hJEkmd.prototype.oIpoLH = function() {
            AEOgJp.MOGook(this.EgMnOO, this.ohKlgh);
            AEOgJp.GKEMcP(this.ohKlgh, this.LDaAFD);
            AEOgJp.cGgNAb(this.ohKlgh);
        };
        hJEkmd.prototype.CmmiDb = function() {
            if (this.NLoMKI[0] != 0 || this.NLoMKI[1] != 0 || this.jndgcA != 0) {
                this.NLoMKI[0] = 0;
                this.NLoMKI[1] = 0;
                this.jndgcA = 0;
                if (this.DpGKGa) {
                    var EjJIlL = this.DpGKGa.GigegA.point.style;
                    EjJIlL.left = '90px';
                    EjJIlL.top = '90px';
                    dLeLMm.MHlIiE(this.DpGKGa.GigegA.angle, 0);
                }
            };
        };
        hJEkmd.prototype.LgMKPO = function() { if (this.DpGKGa) { if (this.DpGKGa.parentNode) { return true; } }; return false; };
        hJEkmd.prototype.IicMnM = function() {
            if (!this.dgCCGa) { return; };
            this.nnDknc = false;
            if (!this.DpGKGa || this.DICEHA != 1) { return; };
            if (!this.DpGKGa.parentNode) { this.dfOJLM.appendChild(this.DpGKGa); };
            this.dNInBK();
        };
        hJEkmd.prototype.HDLfgG = function() { this.nnDknc = false; if (this.DpGKGa) { if (this.DpGKGa.parentNode) { this.DpGKGa.parentNode.removeChild(this.DpGKGa); } }; };
        hJEkmd.prototype.dNInBK = function() {
            if (!this.DpGKGa) { return; };
            if (!this.DpGKGa.parentNode) { return; };
            var gagIcf = dLeLMm.HdMnnH();
            gagIcf[2] -= 90;
            gagIcf[3] -= 90;
            var pMdOJG = AEOgJp.clhoEK(this.NMOOPN);
            this.NOfpPB(pMdOJG);
            AEOgJp.GKEMcP(pMdOJG, this.LDaAFD);
            if (pMdOJG[0] < 90) { pMdOJG[0] = 90; } else if (pMdOJG[0] > gagIcf[2]) { pMdOJG[0] = gagIcf[2]; };
            if (pMdOJG[1] < 90) { pMdOJG[1] = 90; } else if (pMdOJG[1] > gagIcf[3]) { pMdOJG[1] = gagIcf[3]; };
            AEOgJp.cGgNAb(pMdOJG);
            this.DpGKGa.style.left = pMdOJG[0] + 'px';
            this.DpGKGa.style.top = pMdOJG[1] + 'px';
            AEOgJp.pjMFnl(pMdOJG, this.LDaAFD);
            this.DpGKGa.CHAnnH = pMdOJG;
        };
        hJEkmd.prototype.GEIpEh = function(ooLIDD) {
            if (!this.DpGKGa) { return; };
            if (!this.DpGKGa.parentNode) { return; };
            var EjJIlL, kabEIp = this.DpGKGa.CHAnnH;
            var JJlpGf = AEOgJp.IAiaok(kabEIp, ooLIDD);
            if (JJlpGf <= 50) {
                var cfclOK = 30;
                if (JJlpGf > cfclOK) { JJlpGf = cfclOK; };
                AEOgJp.GKEMcP(ooLIDD, kabEIp);
                var MaHImM = AEOgJp.clhoEK(ooLIDD);
                AEOgJp.JIHKfG(MaHImM);
                AEOgJp.obdCcB(MaHImM, JJlpGf);
                AEOgJp.MOGook(MaHImM, ooLIDD);
                AEOgJp.oDoNGM(MaHImM, cfclOK);
                if (MaHImM[0] < -1) { MaHImM[0] = -1; } else if (MaHImM[0] > 1) { MaHImM[0] = 1; };
                if (MaHImM[1] < -1) { MaHImM[1] = -1; } else if (MaHImM[1] > 1) { MaHImM[1] = 1; };
                AEOgJp.MOGook(MaHImM, this.NLoMKI);
                AEOgJp.pjMFnl(ooLIDD, [90, 90]);
                AEOgJp.cGgNAb(ooLIDD);
                EjJIlL = this.DpGKGa.GigegA.point.style;
                EjJIlL.left = ooLIDD[0] + 'px';
                EjJIlL.top = ooLIDD[1] + 'px';
            } else {
                var oiHopF = 0.94;
                var epcBke = HiMfgN.ggiaCo - AEOgJp.EfhfDe(kabEIp, ooLIDD);
                if (epcBke <= (oiHopF + 0.03) && epcBke >= -0.03) {
                    if (epcBke > oiHopF) { epcBke = oiHopF; } else if (epcBke < 0) { epcBke = 0; };
                    this.jndgcA = epcBke / oiHopF;
                    dLeLMm.MHlIiE(this.DpGKGa.GigegA.angle, -epcBke);
                }
            };
        };
        hJEkmd.prototype.iMaEeD = function() { if (this.aMPfEI) { this.aMPfEI.classList.remove('active'); if (this.aMPfEI.parentNode) { this.aMPfEI.parentNode.removeChild(this.aMPfEI); } }; };
        hJEkmd.prototype.fhGCdL = function() {
            if (!this.dgCCGa) { return; };
            if (!this.aMPfEI) {
                this.aMPfEI = BLAZE.DPEkhd.cFgHGM('element', 'game.billiards_spin_button');
                this.aMPfEI.classList.remove('active');
            };
            if (!this.aMPfEI.parentNode) { this.oOJDaI.GigegA.table_markers.appendChild(this.aMPfEI); };
            var GhNgbO = Math.round(this.oDOoFi / MLBlFB * this.cpHPfC + AaKhBc);
            var NOgJOe = Math.round(GhNgbO * -0.5);
            var EjJIlL = this.aMPfEI.style;
            GhNgbO = GhNgbO + 'px';
            EjJIlL.margin = NOgJOe + 'px 0 0 ' + NOgJOe + 'px';
            EjJIlL.width = GhNgbO;
            EjJIlL.height = GhNgbO;
            this.DlIMPP();
            this.aMPfEI.classList.add('active');
        };
        hJEkmd.prototype.DlIMPP = function() {
            if (!this.dgCCGa) { return; };
            if (!this.aMPfEI) { return; };
            if (!this.aMPfEI.parentNode) { return; };
            var hNACfi = dLeLMm.OnKbCc(this.aMPfEI.parentNode);
            var HOCnJf = AEOgJp.clhoEK(this.NMOOPN);
            this.cmfJJm(HOCnJf);
            AEOgJp.GKEMcP(HOCnJf, hNACfi);
            AEOgJp.cGgNAb(HOCnJf);
            var EjJIlL = this.aMPfEI.style;
            EjJIlL.left = HOCnJf[0] + 'px';
            EjJIlL.top = HOCnJf[1] + 'px';
        };
        hJEkmd.prototype.mOCean = function() {
            if (!this.kilLED) { return; };
            this.HDLfgG();
            var cIhEIM = this.GILDeB.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var PfIHKb = this.GILDeB[cJcdCM]; if (PfIHKb.parentNode) { PfIHKb.parentNode.removeChild(PfIHKb); } };
            this.JfDElB = false;
            this.kilLED = null;
        };
        hJEkmd.prototype.AhpMoN = function() {
            if (!this.aPNFBn) { return; };
            var cIhEIM = this.POENJL.length;
            for (var cJcdCM = 0; cJcdCM < cIhEIM; cJcdCM++) { var PfIHKb = this.POENJL[cJcdCM]; if (PfIHKb.parentNode) { PfIHKb.parentNode.removeChild(PfIHKb); } };
            this.aPNFBn = null;
        };
        hJEkmd.prototype.oIFHnl = function(HEFekh, pImeKN) {
            this.mOCean();
            var cJcdCM, ilcBeA, DpfEAC;
            if (!HEFekh) {
                HEFekh = [];
                DpfEAC = this.pEcedm.length;
                for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { HEFekh.push(this.pEcedm[cJcdCM][0]); }
            };
            this.kilLED = HEFekh;
            this.JfDElB = pImeKN;
            var HoolKP = this.oOJDaI.GigegA.table_markers;
            var hNACfi = dLeLMm.OnKbCc(HoolKP);
            var GhNgbO = Math.round(this.oDOoFi / MLBlFB * this.cpHPfC + AaKhBc);
            var NOgJOe = Math.round(GhNgbO * -0.5);
            NOgJOe = NOgJOe + 'px 0 0 ' + NOgJOe + 'px';
            GhNgbO = GhNgbO + 'px';
            var ocONDk = 'BilliardsBallMarker';
            if (pImeKN) { ocONDk = 'BilliardsBallMarkerSelect'; };
            DpfEAC = HEFekh.length;
            for (cJcdCM = this.GILDeB.length; cJcdCM < DpfEAC; cJcdCM++) { this.GILDeB.push(document.createElement('div')); };
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                var JBnmFD = this.KkHaGa(dCibpa(HEFekh[cJcdCM]));
                if (JBnmFD) {
                    if (JBnmFD[1]) {
                        var HOCnJf = AEOgJp.clhoEK(JBnmFD[2]);
                        this.cmfJJm(HOCnJf);
                        AEOgJp.GKEMcP(HOCnJf, hNACfi);
                        AEOgJp.cGgNAb(HOCnJf);
                        var PfIHKb = this.GILDeB[cJcdCM];
                        var EjJIlL = PfIHKb.style;
                        PfIHKb.className = ocONDk;
                        EjJIlL.left = HOCnJf[0] + 'px';
                        EjJIlL.top = HOCnJf[1] + 'px';
                        EjJIlL.width = GhNgbO;
                        EjJIlL.height = GhNgbO;
                        EjJIlL.margin = NOgJOe;
                        HoolKP.appendChild(PfIHKb);
                        if (pImeKN) { AchggF.BPmDoj(PfIHKb, this.KOAIpP, [this, JBnmFD[0]], false); }
                    };
                }
            };
        };
        hJEkmd.prototype.LnMCLM = function(HEFekh) {
            this.AhpMoN();
            this.aPNFBn = HEFekh;
            var HoolKP = this.oOJDaI.GigegA.table_markers;
            var hNACfi = dLeLMm.OnKbCc(HoolKP);
            var GhNgbO = Math.round(BJHIIA * this.cpHPfC);
            var LpCbLj = Math.round(jAhiko * this.cpHPfC);
            if (LpCbLj < 1) { LpCbLj = 1; };
            var NOgJOe = Math.round(GhNgbO * -0.5);
            NOgJOe = NOgJOe + 'px 0 0 ' + NOgJOe + 'px';
            GhNgbO = GhNgbO + 'px';
            var ocONDk = 'BilliardsPocketMarker marker_';
            var cJcdCM, ilcBeA, iBamkN, DpfEAC = HEFekh.length;
            for (cJcdCM = this.POENJL.length; cJcdCM < DpfEAC; cJcdCM++) { this.POENJL.push(document.createElement('div')); };
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                ilcBeA = HEFekh[cJcdCM].split(':');
                if (ilcBeA.length == 2) {
                    var EDBBfo = this.KJoJHA['_' + ilcBeA[0]];
                    if (EDBBfo) {
                        EDBBfo = AEOgJp.clhoEK(EDBBfo);
                        this.cmfJJm(EDBBfo);
                        AEOgJp.GKEMcP(EDBBfo, hNACfi);
                        AEOgJp.cGgNAb(EDBBfo);
                        var PfIHKb = this.POENJL[cJcdCM];
                        var EjJIlL = PfIHKb.style;
                        PfIHKb.className = ocONDk + ilcBeA[1];
                        EjJIlL.left = EDBBfo[0] + 'px';
                        EjJIlL.top = EDBBfo[1] + 'px';
                        EjJIlL.width = GhNgbO;
                        EjJIlL.height = GhNgbO;
                        EjJIlL.margin = NOgJOe;
                        EjJIlL.borderWidth = LpCbLj + 'px';
                        HoolKP.appendChild(PfIHKb);
                    }
                };
            }
        };
        hJEkmd.prototype.KOAIpP = function(fkiijB, fIdnmf) {
            fIdnmf = dCibpa(fIdnmf);
            if (fIdnmf < 0) { return; };
            if (fkiijB.aGEjAM.cOPbiG) { fkiijB.JKdCgI.pPEGkJ({ c: 'chs', v: fIdnmf }); };
            fkiijB.idJgpb(fIdnmf, dCibpa(fkiijB.gLAiKg[1]), dCibpa(fkiijB.gLAiKg[2]), false);
            fkiijB.gLAiKg = null;
            fkiijB.mOCean();
        };
        hJEkmd.prototype.dgcBkM = function(ajJgBK) {
            this.gLAiKg = ajJgBK;
            this.oIFHnl(null, true);
        };
        hJEkmd.prototype.OdlpeC = function() {
            if (this.DICEHA != 1) { return; };
            pgOiDk = this.KkHaGa(this.npEpAb);
            if (!pgOiDk) { return; };
            if (!pgOiDk[1]) { return; };
            var ooLIDD = AEOgJp.clhoEK(this.EgMnOO);
            this.ekPDCM(ooLIDD);
            if (AEOgJp.IAiaok(ooLIDD, pgOiDk[2]) < this.oDOoFi) { this.IicMnM(); return; };
            this.ELlGFH = true;
        };
        hJEkmd.prototype.gmkjGf = function(ooLIDD) {
            if (!this.ELlGFH || this.DICEHA != 1) { return; };
            this.ELlGFH = false;
            pgOiDk = this.KkHaGa(this.npEpAb);
            if (!pgOiDk) { return; };
            if (!pgOiDk[1]) { return; };
            var ooLIDD = AEOgJp.clhoEK(this.EgMnOO);
            var GGidDC = this.CHdncH;
            if (GGidDC > 0.7) { GGidDC = GGidDC * 1.15; } else if (GGidDC < 0.3) { GGidDC = GGidDC * 0.9; };
            if (GGidDC < CFeCBn) { GGidDC = CFeCBn; } else if (GGidDC > 1) { GGidDC = 1; };
            this.ekPDCM(ooLIDD);
            AEOgJp.GKEMcP(ooLIDD, pgOiDk[2]);
            AEOgJp.JIHKfG(ooLIDD);
            AEOgJp.obdCcB(ooLIDD, this.MGOIBg * GGidDC);
            var LpfhDd;
            if (this.dgCCGa) {
                LpfhDd = AEOgJp.clhoEK(this.NLoMKI);
                LpfhDd[2] = this.jndgcA;
                LpfhDd[0] = HiMfgN.cGgNAb(LpfhDd[0] * 1000);
                LpfhDd[1] = HiMfgN.cGgNAb(LpfhDd[1] * 1000);
                LpfhDd[2] = HiMfgN.cGgNAb(LpfhDd[2] * 1000);
            } else { LpfhDd = [0, 0, 0]; };
            this.HeDJeM(this.npEpAb, ooLIDD, LpfhDd, -1, -1, 0);
        };
        hJEkmd.prototype.iJIoEM = function(KcMelf) {
            if (this.nlemFe) { this.GilbBF(); } else {
                if (this.LgMKPO()) { this.HDLfgG(); return; };
                this.EgMnOO[0] = KcMelf.clientX;
                this.EgMnOO[1] = KcMelf.clientY;
                if (this.DICEHA == 1) {
                    KcMelf.preventDefault();
                    KcMelf.stopPropagation();
                    this.oIpoLH();
                    this.OdlpeC();
                    this.MJpbeh();
                }
            };
        };
        hJEkmd.prototype.mPeMFa = function(KcMelf) {
            if (KcMelf.target) { if (KcMelf.target.id.substr(0, 12) == 'videoplayer_' || KcMelf.target.id.substr(0, 16) == 'instagramplayer_') { return; } };
            if (this.LgMKPO()) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.nnDknc = false;
                return;
            };
            this.EgMnOO[0] = KcMelf.clientX;
            this.EgMnOO[1] = KcMelf.clientY;
            if (this.DICEHA == 1) {
                if (KcMelf.target) {
                    KcMelf.preventDefault();
                    KcMelf.stopPropagation();
                    this.oIpoLH();
                    this.gmkjGf();
                }
            } else if (this.moKlIG.ajJgBK) { if (KcMelf.target) { if (KcMelf.target.IgCMNE || KcMelf.target.jOGpoa) { this.eKkChO(); } }; }
        };
        hJEkmd.prototype.LjKKCk = function(KcMelf) {
            if (this.LgMKPO()) { if (this.nnDknc) { this.GEIpEh([KcMelf.clientX, KcMelf.clientY]); }; return; };
            this.EgMnOO[0] = KcMelf.clientX;
            this.EgMnOO[1] = KcMelf.clientY;
            if (this.DICEHA == 1) {
                this.oIpoLH();
                this.MJpbeh();
            } else if (this.moKlIG.ajJgBK) {
                AEOgJp.MOGook(this.EgMnOO, this.moKlIG.ooLIDD);
                this.iFePAm(false, false);
            }
        };
        hJEkmd.prototype.gnkiop = function(KcMelf) {
            if (KcMelf.changedTouches.length < 1) { return; };
            var nJogbk = KcMelf.changedTouches[0];
            if (nJogbk.target) { if (nJogbk.target.id == 'RoomChatInput') { return; } };
            if (this.nlemFe) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.GilbBF();
            } else {
                if (this.LgMKPO()) { this.HDLfgG(); return; };
                this.EgMnOO[0] = nJogbk.clientX;
                this.EgMnOO[1] = nJogbk.clientY;
                if (this.DICEHA == 1) {
                    this.oIpoLH();
                    this.OdlpeC();
                    this.MJpbeh();
                } else if (this.moKlIG.ajJgBK) { if (KcMelf.target) { if (KcMelf.target.IgCMNE || KcMelf.target.jOGpoa) { this.noKAMH(); } }; }
            };
        };
        hJEkmd.prototype.JOcaDM = function(KcMelf) {
            if (this.LgMKPO()) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.nnDknc = false;
                return;
            };
            if (KcMelf.changedTouches.length < 1) { return; };
            var nJogbk = KcMelf.changedTouches[0];
            if (nJogbk.target) { if (nJogbk.target.id == 'RoomChatInput') { return; } };
            this.EgMnOO[0] = nJogbk.clientX;
            this.EgMnOO[1] = nJogbk.clientY;
            if (this.moKlIG.ajJgBK) {
                if (KcMelf.target) {
                    if (KcMelf.target.IgCMNE || KcMelf.target.jOGpoa) {
                        this.eKkChO();
                        KcMelf.preventDefault();
                        KcMelf.stopPropagation();
                    }
                };
            } else if (this.DICEHA == 1) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.oIpoLH();
                this.gmkjGf();
            }
        };
        hJEkmd.prototype.MMGKAO = function(KcMelf) { if (this.LgMKPO()) { this.nnDknc = false; }; if (this.DICEHA == 1) { this.ELlGFH = false; } };
        hJEkmd.prototype.NOEbkC = function(KcMelf) {
            if (KcMelf.changedTouches.length < 1) { return; };
            var nJogbk = KcMelf.changedTouches[0];
            if (this.LgMKPO()) { if (this.nnDknc) { this.GEIpEh([nJogbk.clientX, nJogbk.clientY]); }; return; };
            this.EgMnOO[0] = nJogbk.clientX;
            this.EgMnOO[1] = nJogbk.clientY;
            if (this.DICEHA == 1) {
                this.oIpoLH();
                this.MJpbeh();
            } else if (this.moKlIG.ajJgBK) {
                AEOgJp.MOGook(this.EgMnOO, this.moKlIG.ooLIDD);
                this.iFePAm(false, false);
            }
        };
        hJEkmd.prototype.LhbEgm = function(KcMelf) {
            KcMelf.preventDefault();
            KcMelf.stopPropagation();
        };
        hJEkmd.prototype.dkhnDE = function() { if (!BLAZE.DPEkhd.nJogbk) { this.HDLfgG(); } };
        hJEkmd.prototype.FdePGd = function(KcMelf) {
            if (this.LgMKPO()) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.nnDknc = true;
                this.GEIpEh([KcMelf.clientX, KcMelf.clientY]);
                return;
            }
        };
        hJEkmd.prototype.iMOKhg = function(KcMelf) {
            if (KcMelf.changedTouches.length < 1) { return; };
            var nJogbk = KcMelf.changedTouches[0];
            if (this.LgMKPO()) {
                KcMelf.preventDefault();
                KcMelf.stopPropagation();
                this.nnDknc = true;
                this.GEIpEh([nJogbk.clientX, nJogbk.clientY]);
                return;
            }
        };
        hJEkmd.prototype.hGcmiD = function(EfaoPa, MhGMlH, mfMKCi, FEpbpA, nklAFi) {
            EfaoPa = dCibpa(EfaoPa);
            if (EfaoPa < 0 || EfaoPa > JlCeOh.length - 1) { $error(17992881); return; };
            MhGMlH = dCibpa(MhGMlH);
            mfMKCi = dCibpa(mfMKCi);
            FEpbpA = dCibpa(FEpbpA);
            this.jDPhKk = kPpOoh();
            this.BDKNnM = JlCeOh[EfaoPa];
            this.CaKNNK = dCibpa(nklAFi);
            var cJcdCM, ePoLdm;
            this.mmkIdF(0);
            this.CnAILC();
            this.mOCean();
            this.AhpMoN();
            this.OloiJn.NOjeil();
            this.lNDoji = false;
            this.ccehkL = false;
            var dgnbgf = this.BDKNnM.lcFaFD;
            if (dgnbgf < 0 || dgnbgf > iNcCoK.length - 1) { $error(68909385); return; };
            var fGAilc = this.BDKNnM.GAPjel;
            if (fGAilc < 0 || fGAilc > gOcDCD.length - 1) { $error(40991801); return; };
            var fafiIH = gOcDCD[fGAilc];
            var BMnhpo = this.oOJDaI.GigegA;
            BMnhpo.table_framework.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_framework_' + dgnbgf).src + '")';
            BMnhpo.table_base.style.backgroundImage = 'url("' + BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_default_table').src + '")';
            this.JidbGH = iNcCoK[dgnbgf].AIONko;
            this.khbDkm = { hGehBG: jIbNPl.bGOEmK(iNcCoK[dgnbgf].diBAcc), cPmHPL: jIbNPl.bGOEmK(iNcCoK[dgnbgf].PcpKAg), EMlFPp: [iNcCoK[dgnbgf].IPMfPb[0], iNcCoK[dgnbgf].IPMfPb[1], Math.round(AEOgJp.IAiaok(iNcCoK[dgnbgf].IPMfPb[0], iNcCoK[dgnbgf].IPMfPb[1]) - PEiBck)] };
            this.KJoJHA = iNcCoK[dgnbgf].OMLdpH;
            this.oCoAmj = iNcCoK[dgnbgf].GhfCLm;
            this.hImPiI = iNcCoK[dgnbgf].lLgpbF;
            this.lMPGnH = iNcCoK[dgnbgf].lAAMfE;
            this.NKCCjM = fafiIH.OaahBD;
            this.HHCDAK = fafiIH.OaahBD * MLBlFB;
            this.oDOoFi = this.HHCDAK * 2;
            if (this.CaKNNK == 1) {
                this.MGOIBg = Math.round(this.BDKNnM.FKbhkM * FFkHeK * MLBlFB);
                this.pJeCBO = Math.round(this.BDKNnM.BLPCKm * elpaPi * MLBlFB);
                this.hOlomK = Math.round(this.BDKNnM.BLPCKm * lAAAEb * MLBlFB);
            } else {
                this.MGOIBg = Math.round(this.BDKNnM.FKbhkM * MLBlFB);
                this.hOlomK = Math.round(this.BDKNnM.BLPCKm * MLBlFB);
            };
            this.cDdhDa = Math.round(this.BDKNnM.gfljHJ * MLBlFB);
            dHCPCE = this.oDOoFi;
            ihDbeD = this.oDOoFi * this.oDOoFi;
            this.oGAEIn = {};
            this.pEcedm = [];
            var LHkiKd = BLAZE.DPEkhd.cFgHGM('bitmap', KEfDLO);
            var chDgIo = (fafiIH.OaahBD * 2) / 50;
            var AaIgai = ((fafiIH.OaahBD * 2) / 40) - 0.02;
            var MIkeCN = this.BDKNnM.pEcedm.clone();
            var DpfEAC = MIkeCN.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                ePoLdm = MIkeCN[cJcdCM];
                pgOiDk = [ePoLdm[0], 0, [0, 0],
                    [0, 0],
                    [1, 0], 0
                ];
                var gHppkm = fafiIH.pEcedm[ePoLdm[1]];
                NgBOje = new BLAZE.pEMpHD(LHkiKd, 1, 4, ImeeDd);
                NgBOje.IbAOEi(chDgIo);
                NgBOje.OmMiOf(0);
                this.OloiJn.lnJkFm(-1, NgBOje);
                pgOiDk.push(NgBOje);
                mDaMFE = new BLAZE.pEMpHD(LHkiKd, 1, 4, ImeeDd);
                mDaMFE.IbAOEi(chDgIo);
                mDaMFE.OmMiOf(gHppkm[0]);
                NgBOje.lnJkFm(-1, mDaMFE);
                pgOiDk.push(mDaMFE);
                if (gHppkm[1] < 0) { pgOiDk.push(null); } else {
                    mDaMFE = new BLAZE.pEMpHD(BLAZE.DPEkhd.cFgHGM('bitmap', 'billiards_ballanim_' + gHppkm[1]), 1, 4, mJJNfN);
                    mDaMFE.IbAOEi(AaIgai);
                    mDaMFE.OmMiOf(HiMfgN.jjifcl(0, DMoHbb - 1));
                    mDaMFE.HhMJfk = HiMfgN.jjifcl(0, 359);
                    NgBOje.lnJkFm(-1, mDaMFE);
                    pgOiDk.push(mDaMFE);
                };
                pgOiDk.push(0);
                pgOiDk.push(0);
                pgOiDk.push(null);
                pgOiDk.push([-1, -1, -1, -1, -1, -1, -1]);
                this.pEcedm.push(pgOiDk);
                this.oGAEIn['_' + pgOiDk[0]] = cJcdCM;
                this.AIcGCl(pgOiDk);
            };
            BMnhpo.table_fabric.classList.remove('transition');
            BMnhpo.table_fabric.style.backgroundImage = 'none';
            BMnhpo.table_image.classList.remove('transition');
            BMnhpo.table_image.style.backgroundImage = 'none';
            if (MhGMlH > 0) {
                ePoLdm = 'ttb' + MhGMlH;
                BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, this.Lphbgg, this);
            };
            if (mfMKCi > 0) {
                BMnhpo.table_fabric.style.display = 'block';
                BMnhpo.table_fabric.style.opacity = '0';
                ePoLdm = 'fbr' + mfMKCi;
                BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, this.dOaLbe, this);
            } else { BMnhpo.table_fabric.style.display = 'none'; };
            if (FEpbpA > 0) {
                BMnhpo.table_image.style.display = 'block';
                BMnhpo.table_image.style.opacity = '0';
                ePoLdm = 'tbg' + FEpbpA;
                BLAZE.DPEkhd.heEBin(ePoLdm, aaPJke + ePoLdm + '.png?' + BLAZE.CONTENT_VERSION, 1, this.BoMChg, this);
            } else { BMnhpo.table_image.style.display = 'none'; }
        };
        hJEkmd.prototype.NdfECE = function(ohkCeo) {
            this.JekMGJ = diNKgh.PMNNiO(FHnOoh.gpPaEf(ohkCeo));
            this.JcOhON();
        };
        hJEkmd.prototype.JcOhON = function() {
            var OhEfNB = {};
            var hcAbmJ = [];
            var MIkeCN = this.BDKNnM.pEcedm.clone();
            var iBamkN, ejEapJ, cJcdCM, DpfEAC = MIkeCN.length;
            var OcMDpE = 0;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                iBamkN = MIkeCN.remove(this.JekMGJ[OcMDpE] % MIkeCN.length);
                ejEapJ = iBamkN[0];
                OcMDpE++;
                if (OcMDpE > 15) { OcMDpE = 0; };
                pgOiDk = this.KkHaGa(ejEapJ);
                hcAbmJ.push(pgOiDk);
                OhEfNB['_' + ejEapJ] = cJcdCM;
            };
            this.pEcedm = hcAbmJ;
            this.oGAEIn = OhEfNB;
        };
        hJEkmd.prototype.IGOEpd = function() {
            if (!this.BDKNnM) { $warn(97330684); return; };
            LLFKph.LKkafb('table_setup', 1, false, 0, false);
            this.lNDoji = false;
            this.mmkIdF(0);
            var cJcdCM, knkiEA, CaMbeH, FNdfkp;
            var KGnkFL = this.BDKNnM.KGnkFL * MLBlFB;
            var IFDklk = KGnkFL * 2;
            var KbEdOf = this.BDKNnM.foLokD.clone();
            var AAllJE = {};
            var DdhOHl = [];
            var MIkeCN = this.BDKNnM.pEcedm;
            var DpfEAC = MIkeCN.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                pgOiDk = MIkeCN[cJcdCM];
                CaMbeH = pgOiDk[2];
                if (CaMbeH >= 0) {
                    AAllJE['_' + pgOiDk[0]] = KbEdOf[CaMbeH];
                    KbEdOf[CaMbeH] = null;
                }
            };
            DpfEAC = KbEdOf.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { if (KbEdOf[cJcdCM]) { DdhOHl.push(KbEdOf[cJcdCM]); } };
            var hIgAJC = [1, 1];
            var DpfEAC = this.pEcedm.length;
            var dLONen = 0;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                pgOiDk = this.pEcedm[cJcdCM];
                NgBOje = pgOiDk[6];
                mDaMFE = pgOiDk[7];
                pgOiDk[1] = 1;
                CaMbeH = '_' + pgOiDk[0];
                if (AAllJE[CaMbeH]) { AEOgJp.MOGook(AAllJE[CaMbeH], pgOiDk[2]); } else {
                    knkiEA = DdhOHl.shift();
                    AEOgJp.MOGook(knkiEA, pgOiDk[2]);
                };
                FNdfkp = Math.round(this.JekMGJ[dLONen] / 2.55) * 0.01;
                dLONen++;
                if (dLONen > 15) { dLONen = 0; };
                pgOiDk[2][0] += (IFDklk * FNdfkp) - KGnkFL;
                FNdfkp = Math.round(this.JekMGJ[dLONen] / 2.55) * 0.01;
                dLONen++;
                if (dLONen > 15) { dLONen = 0; };
                pgOiDk[2][1] += (IFDklk * FNdfkp) - KGnkFL;
                NgBOje.hIgAJC = hIgAJC;
                NgBOje.GNDJnF = 1;
                mDaMFE.GNDJnF = 1;
                pgOiDk[3][0] = 0;
                pgOiDk[3][1] = 0;
                pgOiDk[5] = 0;
                if (pgOiDk[8]) {
                    pgOiDk[8].GNDJnF = 1;
                    pgOiDk[8].OmMiOf(HiMfgN.jjifcl(0, DMoHbb - 1));
                    pgOiDk[8].HhMJfk = HiMfgN.jjifcl(0, 359);
                };
                pgOiDk[9] = 0;
                pgOiDk[10] = 0;
                pgOiDk[11] = null;
                this.AIcGCl(pgOiDk);
            };
            this.ccehkL = false;
            this.OloiJn.jeEAJP();
        };
        hJEkmd.prototype.GAmlpF = function(ajJgBK) {
            this.lNDoji = false;
            this.mmkIdF(0);
            var hIgAJC = [1, 1];
            var cJcdCM, DpfEAC = this.pEcedm.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                pgOiDk = this.pEcedm[cJcdCM];
                NgBOje = pgOiDk[6];
                mDaMFE = pgOiDk[7];
                pgOiDk[1] = 0;
                NgBOje.hIgAJC = hIgAJC;
                NgBOje.GNDJnF = 1;
                mDaMFE.GNDJnF = 1;
                pgOiDk[3][0] = 0;
                pgOiDk[3][1] = 0;
                pgOiDk[5] = 0;
                if (pgOiDk[8]) { pgOiDk[8].GNDJnF = 1; };
                pgOiDk[9] = 0;
                pgOiDk[10] = 0;
                pgOiDk[11] = null;
            };
            DpfEAC = ajJgBK.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                var ilcBeA = ajJgBK[cJcdCM].split(';');
                if (ilcBeA.length == 3) {
                    pgOiDk = this.KkHaGa(ilcBeA[0]);
                    if (pgOiDk) {
                        pgOiDk[1] = 1;
                        pgOiDk[2][0] = diNKgh.edFiCc(ilcBeA[1]);
                        pgOiDk[2][1] = diNKgh.edFiCc(ilcBeA[2]);
                    } else { $warn(12069251); }
                } else { $warn(12069252); }
            };
            DpfEAC = this.pEcedm.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { this.AIcGCl(this.pEcedm[cJcdCM]); };
            this.ccehkL = false;
            this.OloiJn.jeEAJP();
        };
        hJEkmd.prototype.aHGMFN = function(fIdnmf, gHFhPn, MIkeCN, GaKfFg) {
            if (!this.BDKNnM) { $warn(88029851); return; };
            gHFhPn = dCibpa(gHFhPn);
            fIdnmf = dCibpa(fIdnmf);
            var JBnmFD = this.KkHaGa(fIdnmf);
            if (!JBnmFD) { $warn(88029852); return; };
            if (!JBnmFD[1]) { $warn(88029853); return; };
            var cJcdCM, DpfEAC;
            var dEeOik = JBnmFD[2];
            var lfGPKj = dCibpa(this.aGEjAM.ePeklC);
            var fafiIH = null;
            if (MIkeCN) {
                fafiIH = {};
                DpfEAC = MIkeCN.length;
                for (var cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { fafiIH['_' + MIkeCN[cJcdCM]] = true; }
            };
            var CcbccN = null;
            if (GaKfFg) {
                CcbccN = {};
                DpfEAC = GaKfFg.length;
                for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { CcbccN['_' + GaKfFg[cJcdCM]] = true; }
            };
            var ifCAna = HiMfgN.cGgNAb(this.oDOoFi * 0.4);
            if (lfGPKj == 0) { cJcdCM = 0.18; } else if (lfGPKj == 1) { cJcdCM = 0.14; } else if (lfGPKj == 2) { cJcdCM = 0.09; };
            var CJLbKc = HiMfgN.cGgNAb(this.oDOoFi - (MLBlFB * HiMfgN.jjifcl(30, 100) * cJcdCM));
            var PlNBBL = [0, 0];
            var GlBMNA = null;
            DpfEAC = this.pEcedm.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                var fbOLNH = this.pEcedm[cJcdCM];
                if (fbOLNH[1]) {
                    if (fbOLNH[0] != fIdnmf) {
                        if (fafiIH) { if (!fafiIH['_' + fbOLNH[0]]) { continue; } };
                        AEOgJp.MOGook(fbOLNH[2], PlNBBL);
                        var AhcAij = AEOgJp.IAiaok(dEeOik, PlNBBL);
                        for (var FjkINp in this.oCoAmj) {
                            if (CcbccN) { if (!CcbccN[FjkINp]) { continue; } };
                            GlBMNA = AEOgJp.GajdDk(PlNBBL, this.oCoAmj[FjkINp]);
                            AEOgJp.JIHKfG(GlBMNA);
                            AEOgJp.obdCcB(GlBMNA, CJLbKc);
                            AEOgJp.pjMFnl(GlBMNA, PlNBBL);
                            if (AhcAij - AEOgJp.IAiaok(dEeOik, GlBMNA) < ifCAna) { continue; };
                            if (this.fOJHoN(dEeOik, GlBMNA, fIdnmf, fbOLNH[0])) { continue; };
                            if (this.fOJHoN(GlBMNA, this.oCoAmj[FjkINp], fbOLNH[0], -1)) { continue; };
                            cJcdCM = DpfEAC;
                            break;
                        }
                    };
                }
            };
            if (!GlBMNA) {
                cJcdCM = ifCAna * 2;
                GlBMNA = PlNBBL;
                if (GlBMNA[0] == 0 && GlBMNA[1] == 0) {
                    GlBMNA = AEOgJp.fCOchd();
                    AEOgJp.pjMFnl(GlBMNA, dEeOik);
                } else { AEOgJp.pjMFnl(GlBMNA, [HiMfgN.jjifcl(0, cJcdCM) - ifCAna, HiMfgN.jjifcl(0, cJcdCM) - ifCAna]); }
            };
            AEOgJp.GKEMcP(GlBMNA, dEeOik);
            AEOgJp.JIHKfG(GlBMNA);
            AEOgJp.obdCcB(GlBMNA, HiMfgN.jjifcl(50, 100) * 0.01 * this.MGOIBg);
            this.HeDJeM(fIdnmf, GlBMNA, [0, 0, 0], gHFhPn, 0, 1);
        };
        hJEkmd.prototype.HeDJeM = function(fIdnmf, KmFGMg, LpfhDd, gHFhPn, iCnNOm, JFDNIc) {
            if (!this.BDKNnM) { $warn(57239481); return; };
            pgOiDk = this.KkHaGa(fIdnmf);
            if (!pgOiDk) { $warn(57239482); return; };
            if (!pgOiDk[1]) { $warn(57239483); return; };
            this.mOCean();
            this.JKdCgI.OEOpEB();
            this.belIOf = fIdnmf;
            this.IbEJMc = 0;
            this.AKflnK = 0;
            this.dJmbaC();
            if (LpfhDd[0] < -1000) { LpfhDd[0] = -1000; } else if (LpfhDd[0] > 1000) { LpfhDd[0] = 1000; };
            if (LpfhDd[1] < -1000) { LpfhDd[1] = -1000; } else if (LpfhDd[1] > 1000) { LpfhDd[1] = 1000; };
            if (LpfhDd[2] < -1000) { LpfhDd[2] = -1000; } else if (LpfhDd[2] > 1000) { LpfhDd[2] = 1000; };
            var BEIBAp = LpfhDd.clone();
            if (BEIBAp[0] == 0 && BEIBAp[1] == 0 && BEIBAp[2] == 0) { pgOiDk[11] = null; } else {
                AEOgJp.JIHKfG(BEIBAp);
                pgOiDk[11] = BEIBAp;
                pgOiDk[11][2] = pgOiDk[11][2] * BEIBAp[0] * 0.00006;
                pgOiDk[11][3] = AEOgJp.EfhfDe([0, 0], BEIBAp);
            };
            AEOgJp.cGgNAb(KmFGMg);
            AEOgJp.MOGook(KmFGMg, pgOiDk[3]);
            AEOgJp.MOGook(pgOiDk[3], pgOiDk[4]);
            AEOgJp.JIHKfG(pgOiDk[4]);
            pgOiDk[5] = HiMfgN.cGgNAb(AEOgJp.FkDjcj(pgOiDk[3]));
            if (pgOiDk[5] > this.MGOIBg) {
                pgOiDk[5] = this.MGOIBg;
                AEOgJp.MOGook(pgOiDk[4], pgOiDk[3]);
                AEOgJp.obdCcB(pgOiDk[3], pgOiDk[5]);
            };
            if (pgOiDk[8]) { pgOiDk[8].HhMJfk = AEOgJp.bPeMEc(pgOiDk[4]); };
            this.idJgpb(fIdnmf, gHFhPn, iCnNOm, true);
            if (JFDNIc > 0) {
                this.lNDoji = true;
                this.CdoEBj.classList.add('autodist');
                window.setTimeout(this.apHdCm, 400, [this, pgOiDk[5]]);
                window.setTimeout(this.kIPnaI, 400, this);
                this.CHdncH = AEOgJp.FkDjcj(KmFGMg) / this.MGOIBg;
                if (this.CHdncH < CFeCBn) { this.CHdncH = CFeCBn; };
                this.nnmpEl();
            } else {
                this.lNDoji = false;
                this.aBJGFj('CjnLhN', pgOiDk[5]);
                this.mmkIdF(EHncnf);
                this.CdoEBj.classList.remove('autodist');
                this.ccehkL = true;
                this.OBIikL.style.top = HiMfgN.cGgNAb(this.cpHPfC * (this.NKCCjM - 5)) + 'px';
            };
            var MGaAbi = AEOgJp.clhoEK(pgOiDk[2]);
            var OpLFEg = AEOgJp.olNCjJ(MGaAbi, pgOiDk[3]);
            if (this.lpPabJ.fhhfhh) {
                var cJcdCM = MGaAbi[1];
                MGaAbi[1] = FibKcf[1] - MGaAbi[0];
                MGaAbi[0] = cJcdCM;
                cJcdCM = OpLFEg[1];
                OpLFEg[1] = FibKcf[1] - OpLFEg[0];
                OpLFEg[0] = cJcdCM;
                this.eDFAeO = AEOgJp.EfhfDe(OpLFEg, MGaAbi);
            } else { this.eDFAeO = AEOgJp.EfhfDe(MGaAbi, OpLFEg); };
            this.OldbdA = false;
            dLeLMm.MHlIiE(this.CdoEBj, this.eDFAeO);
            if (JFDNIc == 0 || JFDNIc == 1) { this.JKdCgI.pPEGkJ({ c: 'shot', v: [fIdnmf, diNKgh.ICGalO(pgOiDk[2][0], 0), diNKgh.ICGalO(pgOiDk[2][1], 0), KmFGMg[0], KmFGMg[1], LpfhDd[0], LpfhDd[1], LpfhDd[2]].join(':') }); }
        };
        hJEkmd.prototype.apHdCm = function(mnfIoP) {
            if (!mnfIoP) { return; };
            mnfIoP[0].aBJGFj('CjnLhN', mnfIoP[1]);
        };
        hJEkmd.prototype.kIPnaI = function(hGbOki) {
            if (!hGbOki.lNDoji) { return; };
            hGbOki.mmkIdF(EHncnf);
            hGbOki.CdoEBj.classList.remove('autodist');
            hGbOki.lNDoji = false;
            hGbOki.ccehkL = true;
            hGbOki.OBIikL.style.top = HiMfgN.cGgNAb(hGbOki.cpHPfC * (hGbOki.NKCCjM - 5)) + 'px';
        };
        hJEkmd.prototype.KkHaGa = function(fIdnmf) {
            fIdnmf = dCibpa(fIdnmf);
            PlaEDm = this.oGAEIn['_' + fIdnmf];
            if (PlaEDm === undefined) { $warn(49005901); return null; };
            pgOiDk = this.pEcedm[PlaEDm];
            if (pgOiDk[0] != fIdnmf) { $warn(49005902); return null; };
            return pgOiDk;
        };
        hJEkmd.prototype.dJmbaC = function() {
            if (this.ccehkL) { $warn(60297738); };
            var OobIPP, DpfEAC = this.pEcedm.length;
            for (var cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                OobIPP = this.pEcedm[cJcdCM][12];
                OobIPP[0] = -1;
                OobIPP[1] = -1;
                OobIPP[2] = -1;
                OobIPP[3] = -1;
                OobIPP[4] = -1;
                OobIPP[5] = -1;
                OobIPP[6] = -1;
            }
        };
        hJEkmd.prototype.hHGnAN = function() { return (kPpOoh() - this.jDPhKk) < 1000; };
        hJEkmd.prototype.PANaGB = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki) { return; };
            if (!hGbOki.DBJhIi) { return; };
            if (NpfeFE && !hGbOki.DBJhIi[pKHmnh]) {
                hGbOki.DBJhIi[pKHmnh] = 'url("' + NpfeFE.src + '")';
                if (hGbOki.DICEHA > 0) {
                    if (hGbOki.GcIhBa === pKHmnh) {
                        hGbOki.GinJoN.style.backgroundImage = hGbOki.DBJhIi[pKHmnh];
                        if (pKHmnh.substring(0, 4) == 'acue') {
                            hGbOki.GinJoN.classList.add('sprite');
                            hGbOki.ngolob.style.backgroundImage = hGbOki.DBJhIi[pKHmnh];
                            var dFNaNi = cmkjdC[dCibpa(pKHmnh.substring(4))];
                            hGbOki.ngolob.style.top = dFNaNi[0] + '%';
                            hGbOki.ngolob.style.bottom = (100 - dFNaNi[0] - 50) + '%';
                            oEfbln.FglKol(hGbOki.ngolob, dFNaNi[3], dFNaNi[1], dFNaNi[2]);
                        } else {
                            hGbOki.GinJoN.classList.remove('sprite');
                            hGbOki.ngolob.style.backgroundImage = '';
                            oEfbln.cdHKBC(hGbOki.ngolob, true);
                        }
                    };
                }
            };
        };
        hJEkmd.prototype.Lphbgg = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki || !NpfeFE) { return; };
            if (!hGbOki.oOJDaI) { return; };
            var hKPAKA = hGbOki.oOJDaI.GigegA.table_base;
            hKPAKA.style.backgroundImage = 'url("' + NpfeFE.src + '")';
        };
        hJEkmd.prototype.dOaLbe = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki || !NpfeFE) { return; };
            if (!hGbOki.oOJDaI) { return; };
            var hKPAKA = hGbOki.oOJDaI.GigegA.table_fabric;
            hKPAKA.style.backgroundImage = 'url("' + NpfeFE.src + '")';
            if (!hGbOki.hHGnAN()) { hKPAKA.classList.add('transition'); };
            hKPAKA.style.opacity = '1';
        };
        hJEkmd.prototype.BoMChg = function(pKHmnh, NpfeFE, hGbOki) {
            if (!hGbOki || !NpfeFE) { return; };
            if (!hGbOki.oOJDaI) { return; };
            var hKPAKA = hGbOki.oOJDaI.GigegA.table_image;
            hKPAKA.style.backgroundImage = 'url("' + NpfeFE.src + '")';
            if (!hGbOki.hHGnAN()) { hKPAKA.classList.add('transition'); };
            hKPAKA.style.opacity = '1';
        };
        hJEkmd.prototype.aeCfaO = function() {
            var Dbdmha = false;
            var cJcdCM, iLEedm, DpfEAC = this.pEcedm.length;
            for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { iLEedm = this.pEcedm[cJcdCM]; if (this.BHJBPn(iLEedm)) { Dbdmha = true; } };
            if (Dbdmha) { this.OloiJn.jeEAJP(); } else if (this.ccehkL) {
                if (this.aGEjAM.cOPbiG) {
                    var OobIPP;
                    var JIcicO = {};
                    JIcicO.a = this.belIOf;
                    var ofMhiD = this.oECmEe[1];
                    if (ofMhiD == 'carom') { pgOiDk = this.KkHaGa(0); if (pgOiDk[1] == 1) { OobIPP = pgOiDk[12]; if (OobIPP[0] > 0) { if (OobIPP[4] == 0) { pgOiDk = this.KkHaGa(1); if (pgOiDk[12][5] == 1) { pgOiDk = this.KkHaGa(2); if (pgOiDk[12][5] == 1) { this.IbEJMc = 1; } }; } }; } } else if (ofMhiD == 'bank') { pgOiDk = this.KkHaGa(0); if (pgOiDk[1] == 1) { OobIPP = pgOiDk[12]; if (OobIPP[0] > 0) { KkIcel = this.KkHaGa(OobIPP[0]); if (KkIcel) { if (KkIcel[1] != 1 && KkIcel[12][1] == 1) { this.IbEJMc = OobIPP[0]; } }; } }; } else if (ofMhiD == 'scoreball') { pgOiDk = this.KkHaGa(0); if (pgOiDk[1] == 1) { OobIPP = pgOiDk[12][6]; if (OobIPP == 23 || OobIPP == 7) { this.IbEJMc = 1; } else if (OobIPP == 6 || OobIPP == 24 || OobIPP == 22 || OobIPP == 8) { this.IbEJMc = 2; } }; };
                    if (this.IbEJMc > 0) { JIcicO.s = this.IbEJMc; };
                    var khFnEl = [];
                    for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) {
                        pgOiDk = this.pEcedm[cJcdCM];
                        OobIPP = pgOiDk[12];
                        if (pgOiDk[1] == 1) {
                            Cignob = pgOiDk[2];
                            khFnEl.push([pgOiDk[0], OobIPP[0], diNKgh.ICGalO(Cignob[0], 0), diNKgh.ICGalO(Cignob[1], 0)].join('#'));
                        } else if (OobIPP[2] >= 0) { khFnEl.push([pgOiDk[0], OobIPP[0], OobIPP[2], OobIPP[3], ''].join('#')); }
                    };
                    JIcicO.b = khFnEl.join('|');
                    this.JKdCgI.pPEGkJ({ c: 'pres', v: JIcicO });
                };
                this.OloiJn.jeEAJP();
                this.ccehkL = false;
                this.pDhCiA();
            }
        };
        hJEkmd.prototype.BHJBPn = function(JBnmFD) {
            if (JBnmFD[1] != 1) {
                if (JBnmFD[10] <= 0) { return false; };
                JBnmFD[10] -= 1;
                this.AIcGCl(JBnmFD);
                return true;
            };
            LgbFPb = JBnmFD[5];
            if (LgbFPb <= 0) { return false; };
            oBNGKp = JBnmFD[3];
            if (LgbFPb <= 0) {
                JBnmFD[11] = null;
                JBnmFD[5] = 0;
                oBNGKp[0] = 0;
                oBNGKp[1] = 0;
                BLAZE.FEEmCf.hJaoNm(JBnmFD[0]);
                return false;
            };
            mDaMFE = JBnmFD[8];
            if (mDaMFE) {
                BpAHoj = HiMfgN.cGgNAb(JBnmFD[9] + LgbFPb);
                IfpeED = BpAHoj % oEAdfk;
                BpAHoj = (BpAHoj - IfpeED) / oEAdfk;
                JBnmFD[9] = IfpeED;
                if (BpAHoj > 0) { mDaMFE.OmMiOf(mDaMFE.CbJPpg() + BpAHoj); } else {
                    if (JBnmFD[10] == 0) { JBnmFD[10] = 1; } else {
                        JBnmFD[10] = 0;
                        JBnmFD[9] = 0;
                        mDaMFE.OmMiOf(mDaMFE.CbJPpg() + 1);
                    }
                };
            };
            AEOgJp.MOGook(JBnmFD[4], oBNGKp);
            AEOgJp.obdCcB(oBNGKp, LgbFPb);
            Cignob = JBnmFD[2];
            ggOFNa = AEOgJp.olNCjJ(Cignob, oBNGKp);
            NiHkDF = [0];
            cGAOBE = 99999999;
            NFehDM = this.lMPGnH[this.NPmPDC(Cignob)][this.NPmPDC(ggOFNa)];
            if (NFehDM) {
                BpAHoj = NFehDM.length;
                for (IfpeED = 0; IfpeED < BpAHoj; IfpeED++) {
                    HGBEdM = this.EBmMkf(NFehDM[IfpeED]);
                    ncckdM = this.jKLPCa(Cignob, ggOFNa, HGBEdM[0], HGBEdM[1]);
                    if (ncckdM) {
                        aFmBin = AEOgJp.IAiaok(Cignob, ncckdM) - MLBlFB;
                        if (aFmBin < 0) { aFmBin = 0; };
                        if (cGAOBE > aFmBin) {
                            cGAOBE = aFmBin;
                            NiHkDF[0] = 1;
                            NiHkDF[1] = HGBEdM[0];
                            NiHkDF[2] = HGBEdM[1];
                            NiHkDF[3] = aFmBin;
                            NiHkDF[4] = NFehDM[IfpeED];
                            NiHkDF[5] = ncckdM;
                        }
                    };
                }
            };
            aOlgBO = JBnmFD[0];
            FKHFNj = LgbFPb + this.oDOoFi + LmbbBH;
            GOCHcG = this.pEcedm;
            BpAHoj = GOCHcG.length;
            for (IfpeED = 0; IfpeED < BpAHoj; IfpeED++) {
                KkIcel = GOCHcG[IfpeED];
                if (KkIcel[1]) {
                    if (KkIcel[0] != aOlgBO) {
                        HGBEdM = this.dKhlAk(cGAOBE, Cignob, ggOFNa, oBNGKp, LgbFPb, KkIcel[2], KkIcel[3]);
                        if (HGBEdM) {
                            cGAOBE = HGBEdM[0];
                            NiHkDF[0] = 2;
                            NiHkDF[1] = HGBEdM;
                            NiHkDF[2] = KkIcel;
                        }
                    };
                }
            };
            if (NiHkDF[0] == 1) {
                if (NiHkDF[1][2] > 0) {
                    this.aBJGFj('lLPBaL', LgbFPb);
                    ggOFNa = this.IJGapa(NiHkDF[1][2]);
                    BLAZE.FEEmCf.cJfcOf(aOlgBO, ggOFNa);
                    AEOgJp.cGgNAb(ggOFNa);
                    AEOgJp.MOGook(ggOFNa, Cignob);
                    JBnmFD[11] = null;
                    JBnmFD[1] = 0;
                    JBnmFD[5] = 0;
                    LgbFPb = 0;
                    JBnmFD[10] = hlKMBI;
                    oBNGKp[0] = 0;
                    oBNGKp[1] = 0;
                    HGBEdM = JBnmFD[6].ooLIDD;
                    AEOgJp.MOGook(JBnmFD[2], HGBEdM);
                    AEOgJp.obdCcB(HGBEdM, OHLmpM);
                    JBnmFD[12][2] = this.AKflnK;
                    JBnmFD[12][3] = NiHkDF[1][2];
                    this.AKflnK++;
                } else {
                    if (JBnmFD[12][0] < 0) { if (JBnmFD[12][6] < 0) { JBnmFD[12][6] = NiHkDF[4]; } };
                    if (JBnmFD[12][1] < 0) { if (NiHkDF[1][0] == NiHkDF[2][0]) { JBnmFD[12][1] = 1; } else if (NiHkDF[1][1] == NiHkDF[2][1]) { JBnmFD[12][1] = 1; } };
                    if (JBnmFD[12][4] < 0) { if (JBnmFD[12][0] >= 0) { JBnmFD[12][4] = 0; } };
                    this.aBJGFj('LbbgNE', LgbFPb);
                    if (JBnmFD[11]) { if (JBnmFD[11][0] != 0) { JBnmFD[11][0] = 0; }; if (JBnmFD[11][1] != 0) { JBnmFD[11][1] = 0; } };
                    ggOFNa = AEOgJp.clhoEK(JBnmFD[4]);
                    AEOgJp.obdCcB(ggOFNa, NiHkDF[3]);
                    AEOgJp.pjMFnl(ggOFNa, Cignob);
                    BLAZE.FEEmCf.aNchdD(aOlgBO, ggOFNa, NiHkDF[5], LgbFPb);
                    this.FfLbiM(JBnmFD, NiHkDF[1], NiHkDF[2]);
                    LgbFPb = LgbFPb - this.cDdhDa;
                    if (LgbFPb <= 0) {
                        LgbFPb = 0;
                        oBNGKp[0] = 0;
                        oBNGKp[1] = 0;
                    } else {
                        AEOgJp.MOGook(JBnmFD[4], oBNGKp);
                        AEOgJp.obdCcB(oBNGKp, LgbFPb);
                        AEOgJp.cGgNAb(oBNGKp);
                    }
                };
            } else if (NiHkDF[0] == 2) {
                BPEjBk = LgbFPb;
                HGBEdM = NiHkDF[1];
                ggOFNa = HGBEdM[1];
                if (JBnmFD[11]) {
                    MlfBNK = LgbFPb;
                    OgCIlK = AEOgJp.clhoEK(JBnmFD[4]);
                };
                AEOgJp.MOGook(HGBEdM[2], oBNGKp);
                AEOgJp.cGgNAb(oBNGKp);
                AEOgJp.MOGook(oBNGKp, JBnmFD[4]);
                AEOgJp.JIHKfG(JBnmFD[4]);
                LgbFPb = HiMfgN.cGgNAb(AEOgJp.FkDjcj(oBNGKp));
                if (JBnmFD[11]) {
                    if (JBnmFD[11][0] != 0 || JBnmFD[11][1] != 0) {
                        NgfpPb = LgbFPb / MlfBNK;
                        LgbFPb = LgbFPb * 0.4 + (MlfBNK * AEOgJp.FkDjcj(JBnmFD[11]) * (1 - NgfpPb) * 0.4);
                        AEOgJp.obdCcB(JBnmFD[4], NgfpPb);
                        AEOgJp.FgEHFp(OgCIlK, JBnmFD[11][3]);
                        AEOgJp.obdCcB(OgCIlK, 1 - NgfpPb);
                        AEOgJp.pjMFnl(JBnmFD[4], OgCIlK);
                        AEOgJp.JIHKfG(JBnmFD[4]);
                        AEOgJp.MOGook(JBnmFD[4], oBNGKp);
                        AEOgJp.obdCcB(oBNGKp, LgbFPb);
                        AEOgJp.cGgNAb(oBNGKp);
                        JBnmFD[11][0] = 0;
                        JBnmFD[11][1] = 0;
                    }
                };
                if (JBnmFD[8]) { if (LgbFPb > MLBlFB) { JBnmFD[8].HhMJfk = AEOgJp.bPeMEc(JBnmFD[4]); } };
                KkIcel = NiHkDF[2];
                if (KkIcel[11]) {
                    MlfBNK = KkIcel[5];
                    OgCIlK = AEOgJp.clhoEK(KkIcel[4]);
                };
                AEOgJp.MOGook(HGBEdM[3], KkIcel[3]);
                AEOgJp.cGgNAb(KkIcel[3]);
                AEOgJp.MOGook(KkIcel[3], KkIcel[4]);
                AEOgJp.JIHKfG(KkIcel[4]);
                KkIcel[5] = HiMfgN.cGgNAb(AEOgJp.FkDjcj(KkIcel[3]));
                if (KkIcel[11]) {
                    if (KkIcel[11][0] != 0 || KkIcel[11][1] != 0) {
                        NgfpPb = KkIcel[5] / MlfBNK;
                        KkIcel[5] = KkIcel[5] * 0.4 + (MlfBNK * AEOgJp.FkDjcj(KkIcel[11]) * (1 - NgfpPb) * 0.4);
                        AEOgJp.obdCcB(KkIcel[4], NgfpPb);
                        AEOgJp.FgEHFp(OgCIlK, KkIcel[11][3]);
                        AEOgJp.obdCcB(OgCIlK, 1 - NgfpPb);
                        AEOgJp.pjMFnl(KkIcel[4], OgCIlK);
                        AEOgJp.JIHKfG(KkIcel[4]);
                        AEOgJp.MOGook(KkIcel[4], KkIcel[3]);
                        AEOgJp.obdCcB(KkIcel[3], KkIcel[5]);
                        AEOgJp.cGgNAb(KkIcel[3]);
                        KkIcel[11][0] = 0;
                        KkIcel[11][1] = 0;
                    }
                };
                if (KkIcel[8]) { if (KkIcel[5] > MLBlFB) { KkIcel[8].HhMJfk = AEOgJp.bPeMEc(KkIcel[4]); } };
                if (LgbFPb > KkIcel[5]) { this.aBJGFj('JBnmFD', LgbFPb); } else { this.aBJGFj('JBnmFD', KkIcel[5]); };
                if (JBnmFD[12][4] < 0) { if (JBnmFD[12][0] >= 0) { JBnmFD[12][4] = 1; } };
                if (KkIcel[12][4] < 0) { if (KkIcel[12][0] >= 0) { KkIcel[12][4] = 1; } };
                if (JBnmFD[12][0] < 0) { JBnmFD[12][0] = KkIcel[0]; };
                if (KkIcel[12][0] < 0) { KkIcel[12][0] = JBnmFD[0]; };
                if (KkIcel[0] == 0) { JBnmFD[12][5] = 1; };
                if (JBnmFD[0] == 0) { KkIcel[12][5] = 1; };
                BLAZE.FEEmCf.kIfOdD(aOlgBO, ggOFNa, KkIcel[0], KkIcel[2], BPEjBk);
            };
            if (JBnmFD[1]) { BLAZE.FEEmCf.ImogkE(aOlgBO, Cignob, ggOFNa, LgbFPb); };
            AEOgJp.cGgNAb(ggOFNa);
            AEOgJp.MOGook(ggOFNa, Cignob);
            if (JBnmFD[11]) {
                AEOgJp.FgEHFp(JBnmFD[4], JBnmFD[11][2] * (LgbFPb / this.MGOIBg));
                AEOgJp.JIHKfG(JBnmFD[4]);
                AEOgJp.MOGook(JBnmFD[4], oBNGKp);
                AEOgJp.obdCcB(oBNGKp, LgbFPb);
                AEOgJp.cGgNAb(oBNGKp);
            };
            if (this.CaKNNK == 1) { LgbFPb = HiMfgN.cGgNAb(LgbFPb - (this.hOlomK + ((LgbFPb / this.MGOIBg) * this.pJeCBO))); } else { LgbFPb = HiMfgN.cGgNAb(LgbFPb - this.hOlomK); };
            JBnmFD[5] = LgbFPb;
            if (JBnmFD[1]) { if (LgbFPb <= 0) { BLAZE.FEEmCf.hJaoNm(aOlgBO); } };
            this.AIcGCl(JBnmFD);
            return true;
        };
        hJEkmd.prototype.AIcGCl = function(JBnmFD) {
            NgBOje = JBnmFD[6];
            mDaMFE = JBnmFD[7];
            if (JBnmFD[1] != 1) {
                if (JBnmFD[10] > 0) {
                    if (!NgBOje.hIHeHD) { NgBOje.hIHeHD = true; };
                    BpAHoj = JBnmFD[10];
                    IfpeED = ahDlEp + ((BpAHoj - 1) * mDGpen);
                    NgBOje.hIgAJC = [IfpeED, IfpeED];
                    IfpeED = LnBhIE * BpAHoj;
                    NgBOje.GNDJnF = IfpeED;
                    mDaMFE.GNDJnF = IfpeED;
                    mDaMFE = JBnmFD[8];
                    if (mDaMFE) { mDaMFE.GNDJnF = IfpeED; }
                } else if (NgBOje.hIHeHD) { NgBOje.hIHeHD = false; }
            } else {
                if (!NgBOje.hIHeHD) { NgBOje.hIHeHD = true; };
                Cignob = NgBOje.ooLIDD;
                AEOgJp.MOGook(JBnmFD[2], Cignob);
                AEOgJp.obdCcB(Cignob, OHLmpM);
            }
        };
        hJEkmd.prototype.NPmPDC = function(ooLIDD) { if (ooLIDD[0] < 0) { ooLIDD = [0, ooLIDD[1]]; } else if (ooLIDD[0] >= FibKcf[0]) { ooLIDD = [FibKcf[0] - MLBlFB, ooLIDD[1]]; }; if (ooLIDD[1] < 0) { ooLIDD = [ooLIDD[0], 0]; } else if (ooLIDD[1] >= FibKcf[1]) { ooLIDD = [ooLIDD[0], FibKcf[1] - MLBlFB]; }; return HiMfgN.dcahnC(ooLIDD[0] / NcFLDH[0]) + HiMfgN.dcahnC(ooLIDD[1] / NcFLDH[1]) * gInEBG[0]; };
        hJEkmd.prototype.EBmMkf = function(pdPKJA) { return [this.hImPiI[pdPKJA], this.hImPiI[pdPKJA + 1]]; };
        hJEkmd.prototype.IJGapa = function(hDHonK) { var iBamkN = this.KJoJHA['_' + hDHonK]; if (!iBamkN) { iBamkN = [0, 0]; }; return iBamkN; };
        hJEkmd.prototype.jKLPCa = function(cCaICn, aHcimf, HBMhoh, HkANed) {
            gnfGKL = aHcimf[1] - cCaICn[1];
            ckOaCH = cCaICn[0] - aHcimf[0];
            hKEiAF = HBMhoh[3];
            PGDjHJ = HBMhoh[4];
            HiLFPf = (gnfGKL * PGDjHJ) - (hKEiAF * ckOaCH);
            if (Math.abs(HiLFPf) == 0) { return null; };
            ckOECA = cCaICn[0] - HBMhoh[0];
            DlmjIn = cCaICn[1] - HBMhoh[1];
            fkHCmP = ckOECA * hKEiAF - DlmjIn * (HkANed[0] - HBMhoh[0]);
            MOdlNl = fkHCmP / -HiLFPf;
            if (MOdlNl < 0 || MOdlNl > 1) { return null; };
            MhflPF = DlmjIn * ckOaCH - ckOECA * (cCaICn[1] - aHcimf[1]);
            EeMCJl = MhflPF / -HiLFPf;
            if (EeMCJl < 0 || EeMCJl > 1) { return null; };
            HpmkkO = (aHcimf[0] * cCaICn[1]) - (cCaICn[0] * aHcimf[1]);
            McklBp = HBMhoh[5];
            return [((ckOaCH * McklBp) - (PGDjHJ * HpmkkO)) / HiLFPf, ((hKEiAF * HpmkkO) - (gnfGKL * McklBp)) / HiLFPf];
        };
        hJEkmd.prototype.FfLbiM = function(JBnmFD, cMdMEN, fdPKLL) {
            fkHCmP = JBnmFD[3];
            MhflPF = cMdMEN[6];
            ckOECA = fdPKLL[0] - cMdMEN[0];
            DlmjIn = fdPKLL[1] - cMdMEN[1];
            HpmkkO = -DlmjIn / MhflPF;
            McklBp = ckOECA / MhflPF;
            HiLFPf = -fkHCmP[0] * HpmkkO - fkHCmP[1] * McklBp;
            JBnmFD[3][0] = fkHCmP[0] + 2 * HpmkkO * HiLFPf;
            JBnmFD[3][1] = fkHCmP[1] + 2 * McklBp * HiLFPf;
            AEOgJp.cGgNAb(JBnmFD[3]);
            AEOgJp.MOGook(JBnmFD[3], JBnmFD[4]);
            AEOgJp.JIHKfG(JBnmFD[4]);
            JBnmFD[5] = HiMfgN.cGgNAb(AEOgJp.FkDjcj(JBnmFD[3]));
            if (JBnmFD[8]) { if (JBnmFD[5] > MLBlFB) { JBnmFD[8].HhMJfk = AEOgJp.bPeMEc(JBnmFD[4]); } };
        };
        hJEkmd.prototype.KnbifO = function(OHBNPj, cMdMEN, fdPKLL) {
            MhflPF = cMdMEN[6];
            ckOECA = fdPKLL[0] - cMdMEN[0];
            DlmjIn = fdPKLL[1] - cMdMEN[1];
            HpmkkO = -DlmjIn / MhflPF;
            McklBp = ckOECA / MhflPF;
            HiLFPf = -OHBNPj[0] * HpmkkO - OHBNPj[1] * McklBp;
            fkHCmP = [OHBNPj[0] + 2 * HpmkkO * HiLFPf, OHBNPj[1] + 2 * McklBp * HiLFPf];
            AEOgJp.JIHKfG(fkHCmP);
            return fkHCmP;
        };
        hJEkmd.prototype.dKhlAk = function(AkfdDD, NcpIIF, LoDGLM, enHCCK, HDEDNp, NPDhFb, dclCOf) {
            Iipemg = AEOgJp.EfhfDe(NcpIIF, NPDhFb) - AEOgJp.dNELFd(enHCCK);
            CcDmKl = AEOgJp.IAiaok(NcpIIF, NPDhFb);
            JgMBLB = Math.sin(Iipemg) * CcDmKl;
            if (JgMBLB <= 0) { return null; };
            if (JgMBLB >= HDEDNp) { if (JgMBLB >= HDEDNp + dHCPCE) { return null; }; if (AEOgJp.IAiaok(LoDGLM, NPDhFb) > dHCPCE) { return null; } };
            MkAkAB = Math.abs(Math.cos(Iipemg) * CcDmKl);
            if (MkAkAB >= dHCPCE) { return null; };
            NpJHCM = Math.sqrt(ihDbeD - MkAkAB * MkAkAB) - LmbbBH;
            if (NpJHCM > JgMBLB || NpJHCM < 0) { NpJHCM = 0; } else { NpJHCM = JgMBLB - NpJHCM; };
            if (AkfdDD < NpJHCM) { return null; };
            if (HDEDNp > 0 && NpJHCM > 0) {
                AFncdg = AEOgJp.clhoEK(enHCCK);
                AEOgJp.obdCcB(AFncdg, (1.0 / HDEDNp) * NpJHCM);
                johhah = AEOgJp.olNCjJ(NcpIIF, AFncdg);
            } else { johhah = AEOgJp.clhoEK(NcpIIF); };
            OgCIlK = AEOgJp.GajdDk(NPDhFb, johhah);
            AEOgJp.oCMmhm(OgCIlK);
            AEOgJp.oDoNGM(OgCIlK, dHCPCE);
            AEOgJp.obdCcB(OgCIlK, (enHCCK[0] - dclCOf[0]) * OgCIlK[0] + (enHCCK[1] - dclCOf[1]) * OgCIlK[1]);
            return [NpJHCM, johhah, AEOgJp.GajdDk(enHCCK, OgCIlK), AEOgJp.olNCjJ(dclCOf, OgCIlK)];
        };
        hJEkmd.prototype.fOJHoN = function(HdKgee, CklJdH, JoLJdm, ogICce) { var cJcdCM, JBnmFD, DpfEAC = this.pEcedm.length; for (cJcdCM = 0; cJcdCM < DpfEAC; cJcdCM++) { JBnmFD = this.pEcedm[cJcdCM]; if (JBnmFD[1]) { if (JBnmFD[0] != JoLJdm && JBnmFD[0] != ogICce) { if (this.HaMJNP(HdKgee, CklJdH, JBnmFD[2])) { return true; } }; } }; return false; };
        hJEkmd.prototype.HaMJNP = function(jcgbkN, NAfgBh, OdJmpK) {
            OgCIlK = AEOgJp.GajdDk(NAfgBh, jcgbkN);
            oBNGKp = AEOgJp.FkDjcj(OgCIlK);
            Iipemg = AEOgJp.EfhfDe(jcgbkN, OdJmpK) - AEOgJp.dNELFd(OgCIlK);
            CcDmKl = AEOgJp.IAiaok(jcgbkN, OdJmpK);
            JgMBLB = Math.sin(Iipemg) * CcDmKl;
            if (JgMBLB <= 0) { return false; };
            if (JgMBLB >= oBNGKp) { if (JgMBLB >= oBNGKp + dHCPCE) { return false; }; if (AEOgJp.IAiaok(NAfgBh, OdJmpK) > dHCPCE) { return false; } };
            MkAkAB = Math.abs(Math.cos(Iipemg) * CcDmKl);
            if (MkAkAB >= dHCPCE) { return false; };
            return true;
        };
        hJEkmd.prototype.ekPDCM = function(HBeboB) {
            var hGFgnI = dLeLMm.OnKbCc(this.oOJDaI);
            if (this.lpPabJ.fhhfhh) { var nbbmGF = dLeLMm.HdMnnH()[2] * 0.5; if (hGFgnI[0] > nbbmGF) { hGFgnI[0] -= this.oOJDaI.offsetHeight; } };
            AEOgJp.GKEMcP(HBeboB, hGFgnI);
            AEOgJp.obdCcB(HBeboB, MLBlFB * (BgGFbP[0] / this.oOJDaI.offsetWidth));
            if (this.lpPabJ.fhhfhh) {
                var cJcdCM = HBeboB[1];
                HBeboB[1] = FibKcf[1] - HBeboB[0];
                HBeboB[0] = cJcdCM;
            };
            AEOgJp.cGgNAb(HBeboB);
        };
        hJEkmd.prototype.NOfpPB = function(HBeboB) {
            var hGFgnI = dLeLMm.OnKbCc(this.oOJDaI);
            if (this.lpPabJ.fhhfhh) {
                var nbbmGF = dLeLMm.HdMnnH()[2] * 0.5;
                if (hGFgnI[0] > nbbmGF) { hGFgnI[0] -= this.oOJDaI.offsetHeight; };
                var cJcdCM = HBeboB[0];
                HBeboB[0] = FibKcf[1] - HBeboB[1];
                HBeboB[1] = cJcdCM;
            };
            AEOgJp.oDoNGM(HBeboB, MLBlFB * (BgGFbP[0] / this.oOJDaI.offsetWidth));
            AEOgJp.pjMFnl(HBeboB, hGFgnI);
            AEOgJp.cGgNAb(HBeboB);
        };
        hJEkmd.prototype.cmfJJm = function(HBeboB) {
            var hGFgnI = dLeLMm.OnKbCc(this.oOJDaI);
            AEOgJp.oDoNGM(HBeboB, MLBlFB * (BgGFbP[0] / this.oOJDaI.offsetWidth));
            AEOgJp.pjMFnl(HBeboB, hGFgnI);
            AEOgJp.cGgNAb(HBeboB);
        };
        hJEkmd.prototype.aBJGFj = function(geFmem, iKpDNj) {
            if (this.naNdBk >= FcKhHG) { return; };
            this.naNdBk++;
            iKpDNj = iKpDNj / this.MGOIBg;
            if (geFmem == 'JBnmFD') {
                if (iKpDNj > 0.7) { geFmem = 'jkhnCa'; } else if (iKpDNj > 0.3) {
                    iKpDNj += 0.3;
                    geFmem = 'NOmIgn';
                } else {
                    iKpDNj = iKpDNj * 2 + 0.2;
                    geFmem = 'cFaMeP';
                }
            } else if (geFmem == 'lLPBaL') { iKpDNj += 0.2; } else if (geFmem == 'CjnLhN') { if (iKpDNj < 0.2) { iKpDNj = 0.2; } };
            this.epjIDf(geFmem, iKpDNj);
        };
        hJEkmd.prototype.epjIDf = function(geFmem, OeNLhK) { var HEFekh = MmhAhP[geFmem]; if (!HEFekh) { $warn(geFmem); return; }; if (OeNLhK > 0.85) { OeNLhK = 1; } else if (OeNLhK < 0.15) { return; }; if (HEFekh.length == 1) { LLFKph.LKkafb(HEFekh[0], OeNLhK, false, 0, false); } else { LLFKph.LKkafb(HEFekh.random(), OeNLhK, false, 0, false); } };
        return function() { return new aGEjAM(new hJEkmd(arguments)) };
    })();
    BLAZE.ojABhi = ojABhi;
})(BLAZE || (BLAZE = {}));clear()
